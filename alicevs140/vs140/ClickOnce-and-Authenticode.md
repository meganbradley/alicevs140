---
title: "ClickOnce and Authenticode"
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
ms.assetid: ab5b6712-f32a-4e33-842f-e88ab4818ccf
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ClickOnce and Authenticode
*Authenticode* is a Microsoft technology that uses industry-standard cryptography to sign application code with digital certificates that verify the authenticity of the application's publisher. By using Authenticode for application deployment, [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] reduces the risk of a Trojan horse. A Trojan horse is a virus or other harmful program that a malicious third party misrepresents as a legitimate program coming from an established, trustworthy source. Signing [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] deployments with a digital certificate is an optional step to verify that the assemblies and files are not tampered.  
  
 The following sections describe the different types of digital certificates used in Authenticode, how certificates are validated using Certificate Authorities (CAs), the role of time-stamping in certificates, and the methods of storage available for certificates.  
  
## Authenticode and Code Signing  
 A *digital certificate* is a file that contains a cryptographic public/private key pair, along with metadata describing the publisher to whom the certificate was issued and the agency that issued the certificate.  
  
 There are various types of Authenticode certificates. Each one is configured for different types of signing. For [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications, you must have an Authenticode certificate that is valid for code signing. If you attempt to sign a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application with another type of certificate, such as a digital e-mail certificate, it will not work. For more information, see [Introduction to Code Signing](http://go.microsoft.com/fwlink/?LinkId=179452).  
  
 You can obtain a certificate for code signing in one of three ways:  
  
-   Purchase one from a certificate vendor.  
  
-   Receive one from a group in your organization responsible for creating digital certificates.  
  
-   Generate your own certificate with MakeCert.exe, which is included with the [!INCLUDE[winsdklong](../vs140/includes/winsdklong_md.md)].  
  
### How Using Certificate Authorities Helps Users  
 A certificate generated using the MakeCert.exe utility is commonly called a *self-cert* or a *test cert*. This kind of certificate works much the same way that a .snk file works in the .NET Framework. It consists solely of a public/private cryptographic key pair, and contains no verifiable information about the publisher. You can use self-certs to deploy [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications with high trust on an intranet. However, when these applications run on a client computer, [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] will identify them as coming from an Unknown Publisher. By default, [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications signed with self-certs and deployed over the Internet cannot utilize Trusted Application Deployment.  
  
 By contrast, if you receive a certificate from a CA, such as a certificate vendor, or a department within your enterprise, the certificate offers more security for your users. It not only identifies the publisher of the signed software, but it verifies that identity by checking with the CA that signed it. If the CA is not the root authority, Authenticode will also "chain" back to the root authority to verify that the CA is authorized to issue certificates. For greater security, you should use a certificate issued by a CA whenever possible.  
  
 For more information about generating self-certs, see [Certificate Creation Tool (Makecert.exe)](assetId:///b0343f8e-9c41-4852-a85c-f8a0c408cf0d).  
  
### Timestamps  
 The certificates used to sign [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications expire after a certain length of time, typically twelve months. In order to remove the need to constantly re-sign applications with new certificates, [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] supports timestamp. When an application is signed with a timestamp, its certificate will continue to be accepted even after expiration, provided the timestamp is valid. This allows [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications with expired certificates, but valid timestamps, to download and run. It also allows installed applications with expired certificates to continue to download and install updates.  
  
 To include a timestamp in an application server, a timestamp server must be available. For information about how to select a timestamp server, see [How To: Sign Application and Deployment Manifests](../vs140/How-to--Sign-Application-and-Deployment-Manifests.md).  
  
### Updating Expired Certificates  
 In earlier versions of the .NET Framework, updating an application whose certificate had expired could cause that application to stop functioning. To resolve this problem, use one of the following methods:  
  
-   Update the .NET Framework to version 2.0 SP1 or later on Windows XP, or version 3.5 or later on Windows Vista.  
  
-   Uninstall the application, and reinstall a new version with a valid certificate.  
  
-   Create a command-line assembly that updates the certificate. Step-by-step information about this process can be found at [Microsoft Support Article 925521](http://go.microsoft.com/fwlink/?LinkId=179454).  
  
### Storing Certificates  
  
-   You can store certificates as a .pfx file on your file system, or you can store them inside of a key container. A user on a Windows domain can have a number of key containers. By default, MakeCert.exe will store certificates in your personal key container, unless you specify that it should save it to a .pfx instead. Mage.exe and MageUI.exe, the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)] tools for creating [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] deployments, enable you to use certificates stored in either fashion.  
  
## See Also  
 [ClickOnce Security and Deployment](../Topic/ClickOnce%20Security%20and%20Deployment.md)   
 [ClickOnce Deployment and Security](../vs140/Securing-ClickOnce-Applications.md)   
 [Trusted Application Deployment Overview](../Topic/Trusted%20Application%20Deployment%20Overview.md)   
 [Manifest Generation and Editing Tool (Mage.exe)](assetId:///77dfe576-2962-407e-af13-82255df725a1)