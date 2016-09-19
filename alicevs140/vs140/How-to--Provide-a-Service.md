---
title: "How to: Provide a Service"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 12bc1f12-47b1-44f6-b8db-862aa88d50d1
caps.latest.revision: 24
translation.priority.mt: 
  - de-de
  - ja-jp
---
# How to: Provide a Service
A VSPackage can provide services that other VSPackages can use. To provide a service, a VSPackage must register the service with Visual Studio and add the service.  
  
 The <xref:Microsoft.VisualStudio.Shell.Package?qualifyHint=False> class implements both <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider?qualifyHint=False> and <xref:System.ComponentModel.Design.IServiceContainer?qualifyHint=False>. <xref:System.ComponentModel.Design.IServiceContainer?qualifyHint=False> contains callback methods that provide  services on demand.  
  
 For more information about services, see [Service Essentials](../Topic/Service%20Essentials.md) .  
  
> [!NOTE]
>  When a VSPackage is about to be unloaded, Visual Studio waits until all requests for services that a VSPackage provides have been delivered. It does not allow new requests for these services. You should not explicitly call the <xref:Microsoft.VisualStudio.Shell.Interop.IProfferService.RevokeService?qualifyHint=False> method to revoke a service when unloading.  
  
#### Implementing a service  
  
1.  Create a VSIX project (**File / New / Project / Visual C# / Extensiblity / VSIX Project**).  
  
2.  Add a VSPackage to the project. Select the project node in the **Solution Explorer** and click **Add / New item / Visual C# Items / Extensibility / Visual Studio Package**.  
  
3.  To implement a service, you need to create three types:  
  
    -   An interface that describes the service. Many of these interfaces are empty, that is, they have no methods.  
  
    -   An interface that describes the service interface. This interface includes the methods to be implemented.  
  
    -   A class that implements both the service and the service interface.  
  
     The following example shows a very basic implementation of the three types. The constructor of the service class must set the service provider.  
  
    ```c#  
    public class MyService : SMyService, IMyService  
    {  
        private Microsoft.VisualStudio.OLE.Interop.IServiceProvider serviceProvider;  
        private string myString;  
        public MyService(Microsoft.VisualStudio.OLE.Interop.IServiceProvider sp)  
        {  
            Trace.WriteLine(  
                   "Constructing a new instance of MyService");  
            serviceProvider = sp;  
        }  
        public void Hello()  
        {  
            myString = "hello";  
        }  
        public string Goodbye()  
        {  
           return "goodbye";  
        }  
    }  
    public interface SMyService  
    {  
    }  
    public interface IMyService  
    {  
        void Hello();  
        string Goodbye();  
    }  
  
    ```  
  
### Registering a service  
  
1.  To register a service, add the <xref:Microsoft.VisualStudio.Shell.ProvideServiceAttribute?qualifyHint=False> to the VSPackage that provides the service. Here is an example:  
  
    ```c#  
    [ProvideService(typeof(SMyService))]  
    [PackageRegistration(UseManagedResourcesOnly = true)]  
    [Guid(VSPackage1.PackageGuidString)]  
    public sealed class VSPackage1 : Package  
    {. . . }  
    ```  
  
     This attribute registers `SMyService` with Visual Studio.  
  
    > [!NOTE]
    >  To register a service that replaces another service with the same name, use the <xref:Microsoft.VisualStudio.Shell.ProvideServiceOverrideAttribute?qualifyHint=False>. Note that only one override of a service is allowed.  
  
### Adding a Service  
  
1.  1.  In the VSPackage initializer, add the service and add a callback method to create the services. Here is the change to make to the <xref:Microsoft.VisualStudio.Shell.Package.Initialize?qualifyHint=False> method:  
  
    ```c#  
    protected override void Initialize()  
    {  
        ServiceCreatorCallback callback =new ServiceCreatorCallback(CreateService);  
  
        ((IServiceContainer)this).AddService(typeof(SMyService), callback);  
    . . .  
    }  
    ```  
  
2.  Implement the callback method, which should create and return the service, or null if it cannot be created.  
  
    ```  
    private object CreateService(IServiceContainer container, Type serviceType)  
    {  
        if (typeof(SMyService) == serviceType)  
            return new SMyService(this);  
        return null;  
    }  
    ```  
  
    > [!NOTE]
    >  Visual Studio can reject a request to provide a service. It does so if another VSPackage already provides the service.  
  
3.  Now you can get the service and use its methods. We’ll show this in the initializer, but you can get the service anywhere you want to use the service.  
  
    ```c#  
    protected override void Initialize()  
    {  
        ServiceCreatorCallback callback =new ServiceCreatorCallback(CreateService);  
  
        ((IServiceContainer)this).AddService(typeof(SMyService), callback);  
  
        MyService myService = (MyService) this.GetService(typeof(SMyService));  
        myService.Hello();  
        string helloString = myService.myString;  
  
        base.Initialize();  
    }  
    ```  
  
     The value of `helloString` should be “Hello”.  
  
## See Also  
 [How to: Consume a Service (C#)](../Topic/How%20to:%20Get%20a%20Service.md)   
 [Services](../Topic/Using%20and%20Providing%20Services.md)   
 [Service Essentials](../Topic/Service%20Essentials.md)