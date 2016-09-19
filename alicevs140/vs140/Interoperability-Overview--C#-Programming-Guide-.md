---
title: "Interoperability Overview (C# Programming Guide)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c025b2e0-2357-4c27-8461-118f0090aeff
caps.latest.revision: 45
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Interoperability Overview (C# Programming Guide)
The topic describes methods to enable interoperability between C# managed code and unmanaged code.  
  
## Platform Invoke  
 *Platform invoke* is a service that enables managed code to call unmanaged functions that are implemented in dynamic link libraries (DLLs), such as those in the Microsoft Win32 API. It locates and invokes an exported function and marshals its arguments (integers, strings, arrays, structures, and so on) across the interoperation boundary as needed.  
  
 For more information, see [Consuming Unmanaged DLL Functions](assetId:///eca7606e-ebfb-4f47-b8d9-289903fdc045) and [How to: Use Platform Invoke to Play a Wave File (C# Programming Guide)](../Topic/How%20to:%20Use%20Platform%20Invoke%20to%20Play%20a%20Wave%20File%20\(C%23%20Programming%20Guide\).md).  
  
> [!NOTE]
>  The [Common Language Runtime](assetId:///059a624e-f7db-4134-ba9f-08b676050482) (CLR) manages access to system resources. Calling unmanaged code that is outside the CLR bypasses this security mechanism, and therefore presents a security risk. For example, unmanaged code might call resources in unmanaged code directly, bypassing CLR security mechanisms. For more information, see [.NET Framework Security](http://go.microsoft.com/fwlink/?LinkId=37122).  
  
## C++ Interop  
 You can use C++ interop, also known as It Just Works (IJW), to wrap a native C++ class so that it can be consumed by code that is authored in C# or another .NET Framework language. To do this, you write C++ code to wrap a native DLL or COM component. Unlike other .NET Framework languages, [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] has interoperability support that enables managed and unmanaged code to be located in the same application and even in the same file. You then build the C++ code by using the **/clr** compiler switch to produce a managed assembly. Finally, you add a reference to the assembly in your C# project and use the wrapped objects just as you would use other managed classes.  
  
## Exposing COM Components to C#  
 You can consume a COM component from a C# project. The general steps are as follows:  
  
1.  Locate a COM component to use and register it. Use regsvr32.exe to register or un–register a COM DLL.  
  
2.  Add to the project a reference to the COM component or type library.  
  
     When you add the reference, [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] uses the [Type Library Importer (Tlbimp.exe)](assetId:///ec0a8d63-11b3-4acd-b398-da1e37e97382), which takes a type library as input, to output a .NET Framework interop assembly. The assembly, also named a runtime callable wrapper (RCW), contains managed classes and interfaces that wrap the COM classes and interfaces that are in the type library. [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] adds to the project a reference to the generated assembly.  
  
3.  Create an instance of a class that is defined in the RCW. This, in turn, creates an instance of the COM object.  
  
4.  Use the object just as you use other managed objects. When the object is reclaimed by garbage collection, the instance of the COM object is also released from memory.  
  
 For more information, see [Exposing COM Components to the .NET Framework](assetId:///e78b14f1-e487-43cd-9c6d-1a07483f1730).  
  
## Exposing C# to COM  
 COM clients can consume C# types that have been correctly exposed. The basic steps to expose C# types are as follows:  
  
1.  Add interop attributes in the C# project.  
  
     You can make an assembly COM visible by modifying [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] project properties. For more information, see [Assembly Information Dialog Box](../Topic/Assembly%20Information%20Dialog%20Box.md).  
  
2.  Generate a COM type library and register it for COM usage.  
  
     You can modify [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] project properties to automatically register the C# assembly for COM interop. [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] uses the [Assembly Registration Tool (Regasm.exe)](assetId:///e190e342-36ef-4651-a0b4-0e8c2c0281cb), using the `/tlb` command-line switch, which takes a managed assembly as input, to generate a type library. This type library describes the `public` types in the assembly and adds registry entries so that COM clients can create managed classes.  
  
 For more information, see [Exposing .NET Framework Components to COM](assetId:///e42a65f7-1e61-411f-b09a-aca1bbce24c6) and [Example COM Class (C# Programming Guide)](../vs140/Example-COM-Class--C#-Programming-Guide-.md).  
  
## See Also  
 [Improving Interop Performance](http://go.microsoft.com/fwlink/?LinkId=99564)   
 [Introduction to COM Interop](http://go.microsoft.com/fwlink/?LinkId=112406)   
 [Marshaling between Managed and Unmanaged Code](http://go.microsoft.com/fwlink/?LinkId=112398)   
 [Interoperating with Unmanaged Code](assetId:///ccb68ce7-b0e9-4ffb-839d-03b1cd2c1258)   
 [Advanced COM Interoperability](assetId:///3ada36e5-2390-4d70-b490-6ad8de92f2fb)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)