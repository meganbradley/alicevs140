---
title: "Securing ClickOnce Applications"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-deployment
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a05b5f2f-d1f2-471a-8096-8b11f7554265
caps.latest.revision: 47
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Securing ClickOnce Applications
[!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications are subject to code access security constraints in the .NET Framework to help limit the access that code has to protected resources and operations. For that reason, it is important that you understand the implications of code access security to write your [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications accordingly. Your applications can use Full Trust or use partial zones, such as the Internet and Intranet zones, to limit access.  
  
 Additionally, ClickOnce uses certificates to verify the authenticity of the application's publisher, and to sign the application and deployment manifests to prove that the files have not been tampered with. Signing is an optional step, which makes it easier to change the application files after the manifests are generated. However, without signed manifests, it is difficult to ensure that the application installer is not tampered in man-in-the-middle security attacks. For this reason, we recommend that you sign your application and deployment manifests to help secure your applications.  
  
## Zones  
 Applications that are deployed using [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] technology are restricted to a set of permissions and actions that are defined by the security zone. Security zones are defined in Internet Explorer, and are based on the location of the application. The following table lists the default permissions based on the deployment location:  
  
|Deployment Location|Security Zone|  
|-------------------------|-------------------|  
|Run from Web|Internet Zone|  
|Install from Web|Internet Zone|  
|Install from network file share|Local Intranet Zone|  
|Install from CD-ROM|Full Trust|  
  
 The default permissions are based on the location from which the original version of the application was deployed; updates to the application will inherit those permissions. If the application is configured to check for updates from a Web or network location and a newer version is available, the original installation can receive permissions for the Internet or Intranet zone instead of full-trust permissions. To prevent users from being prompted, a System Administrator can specify a ClickOnce deployment policy that defines a specific application publisher as a trusted source. For computers on which this policy is deployed, permissions will be granted automatically and the user will not be prompted. For more information, see [Trusted Application Deployment Overview](../Topic/Trusted%20Application%20Deployment%20Overview.md). To configure trusted application deployment, the certificate can be installed to the machine or enterprise level. For more information, see [How to: Add a Trusted Publisher to a Client Computer for ClickOnce Applications](../Topic/How%20to:%20Add%20a%20Trusted%20Publisher%20to%20a%20Client%20Computer%20for%20ClickOnce%20Applications.md).  
  
## Code Access Security Policies  
 Permissions for an application are determined by the settings in the [<TrustInfo\> Element](../Topic/%3CtrustInfo%3E%20Element%20\(ClickOnce%20Application\).md) element of the application manifest. [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] automatically generates this information based on the settings on the project's **Security** property page. A [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application is granted only the specific permissions that it requests. For example, where file access requires full-trust permissions, if the application requests file-access permission, it will only be granted file-access permission, not full-trust permissions. When developing your [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application, you should make sure that you request only the specific permissions that the application needs. In most cases, you can use the Internet or Local Intranet zones to limit your application to partial trust. For more information, see [How to: Set a Security Zone for a ClickOnce Application](../vs140/How-to--Set-a-Security-Zone-for-a-ClickOnce-Application.md). If your application requires custom permissions, you can create a custom zone. For more information, see [How to: Set Custom Permissions for a ClickOnce Application](../Topic/How%20to:%20Set%20Custom%20Permissions%20for%20a%20ClickOnce%20Application.md).  
  
 Including a permission that is not part of the default permission set for the zone from which the application is deployed will cause the end user to be prompted to grant permission at install or update time. To prevent users from being prompted, a system administrator can specify a ClickOnce deployment policy that defines a specific application publisher as a trusted source. On computers where this policy is deployed, permissions will automatically be granted and the user will not be prompted.  
  
 As a developer, it is your responsibility to make sure that your application will run with the appropriate permissions. If the application requests permissions outside of a zone during run time, a security exception may appear. [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] enables you to debug your application in the target security zone. and provides help in developing secure applications. For more information, see [How to: Debug a ClickOnce Application with Restricted Permissions](../vs140/How-to--Debug-a-ClickOnce-Application-with-Restricted-Permissions.md).  
  
 For more information about code access security and ClickOnce, see [Code Access Security for ClickOnce Applications](../Topic/Code%20Access%20Security%20for%20ClickOnce%20Applications.md).  
  
## Code-Signing Certificates  
 To publish an application by using [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] deployment, you can sign the application and deployment manifests for the application by using a public/private key pair. The tools for signing a manifest are available on the **Signing** page of the **Project Designer**. For more information, see [Signing Page, Project Designer](../vs140/Signing-Page--Project-Designer.md). Alternatively, you can sign the manifests with a key file during the publishing process, using the Publish Wizard.  
  
 After the manifests are signed, the publisher information based on the Authenticode signature will be displayed to the user in the permissions dialog box during installation, to show the user that the application originated from a trusted source.  
  
 For more information about ClickOnce and certificates, see [ClickOnce and Authenticode](../vs140/ClickOnce-and-Authenticode.md).  
  
## ASP.NET Form-Based Authentication  
 If you want to control which deployments each user can access, you should not enable anonymous access to [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications deployed on a Web server. Rather, you would enable users access to the deployments you have installed based on a user's identity using Windows authentication.  
  
 [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] does not support ASP.NET forms-based authentication because it uses persistent cookies; these present a security risk because they reside in the Internet Explorer cache and can be hacked. Therefore, if you are deploying [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications, any authentication scenario besides Windows authentication is unsupported.  
  
## Passing Arguments  
 An additional security consideration occurs if you have to pass arguments into a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application. [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] enables developers to supply a query string to applications deployed over the Web. The query string takes the form of a series of name-value pairs at the end of the URL used to start the application:  
  
 `http://servername.adatum.com/WindowsApp1.application?username=joeuser`  
  
 By default, query-string arguments are disabled. To enable them, the attribute `trustUrlParameters` must be set in the application's deployment manifest. This value can be set from [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] and from MageUI.exe. For detailed steps on how to enable passing query strings, see [How to: Retrieve Query String Information in a ClickOnce Application](../Topic/How%20to:%20Retrieve%20Query%20String%20Information%20in%20an%20Online%20ClickOnce%20Application.md).  
  
 You should never pass arguments retrieved through a query string to a database or to the command line without checking the arguments to make sure that they are safe. Unsafe arguments are ones that include database or command line escape characters that could allow a malicious user to manipulate your application into executing arbitrary commands.  
  
> [!NOTE]
>  Query-string arguments are the only way to pass arguments to a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application at startup. You cannot pass arguments to a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application from the command line.  
  
## Deploying Obfuscated Assemblies  
 You might want to obfuscate your application by using Dotfuscator to prevent others from reverse engineering the code. However, assembly obfuscation is not integrated into the Visual Studio IDE or the ClickOnce deployment process. Therefore, you will have to perform the obfuscation outside of the deployment process, perhaps using a post-build step. After you build the project, you would perform the following steps manually, outside of Visual Studio:  
  
1.  Perform the obfuscation by using Dotfuscator.  
  
2.  Use Mage.exe or MageUI.exe to generate the ClickOnce manifests and sign them. For more information, see [Manifest Generation and Editing Tool (Mage.exe)](assetId:///77dfe576-2962-407e-af13-82255df725a1) and [Manifest Generation and Editing Tool, Graphical Client (MageUI.exe)](assetId:///f9e130a6-8117-49c4-839c-c988f641dc14).  
  
3.  Manually publish (copy) the files to your deployment source location (Web server, UNC share, or CD-ROM).  
  
## See Also  
 [ClickOnce Security and Deployment](../Topic/ClickOnce%20Security%20and%20Deployment.md)   
 [Choosing a ClickOnce Deployment Strategy](../vs140/Choosing-a-ClickOnce-Deployment-Strategy.md)