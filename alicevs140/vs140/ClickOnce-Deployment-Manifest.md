---
title: "ClickOnce Deployment Manifest"
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
ms.assetid: 8457e615-e3b6-4990-8dcf-11bc590e4e9b
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ClickOnce Deployment Manifest
A deployment manifest is an XML file that describes a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] deployment, including the identification of the current [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application version to deploy.  
  
 Deployment manifests have the following elements and attributes.  
  
|Element|Description|Attributes|  
|-------------|-----------------|----------------|  
|[<assembly\> Element](../vs140/-assembly--Element--ClickOnce-Deployment-.md)|Required. Top-level element.|`manifestVersion`|  
|[<assemblyIdentity\> Element](../vs140/-assemblyIdentity--Element--ClickOnce-Deployment-.md)|Required. Identifies the application manifest for the [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application.|`name`<br /><br /> `version`<br /><br /> `publicKeyToken`<br /><br /> `processorArchitecture`<br /><br /> `culture`|  
|[<description\> Element](../vs140/-description--Element--ClickOnce-Deployment-.md)|Required. Identifies application information used to create a shell presence and the **Add or Remove Programs** item in Control Panel.|`publisher`<br /><br /> `product`<br /><br /> `supportUrl`|  
|[<deployment\> Element](../Topic/%3Cdeployment%3E%20Element%20\(ClickOnce%20Deployment\).md)|Optional. Identifies the attributes used for the deployment of updates and exposure to the system.|`install`<br /><br /> `minimumRequiredVersion`<br /><br /> `mapFileExtensions`<br /><br /> `disallowUrlActivation`<br /><br /> `trustUrlParameters`|  
|[<compatibleFrameworks\> Element](../vs140/-compatibleFrameworks--Element--ClickOnce-Deployment-.md)|Required. Identifies the versions of the .NET Framework where this application can install and run.|`SupportUrl`|  
|[<dependency\> Element](../vs140/-dependency--Element--ClickOnce-Deployment-.md)|Required. Identifies the version of the application to install for the deployment and the location of the application manifest.|`preRequisite`<br /><br /> `visible`<br /><br /> `dependencyType`<br /><br /> `codebase`<br /><br /> `size`|  
|[<publisherIdentity\> Element](../vs140/-publisherIdentity--Element--ClickOnce-Deployment-.md)|Required for signed manifests. Contains information about the publisher that signed this deployment manifest.|`Name`<br /><br /> `issuerKeyHash`|  
|[<Signature\> Element](../vs140/-Signature--Element--ClickOnce-Deployment-.md)|Optional. Contains the necessary information to digitally sign this deployment manifest.|None|  
|[<customErrorReporting\> Element](../vs140/-customErrorReporting--Element--ClickOnce-Deployment-.md)|Optional. Specifies a URI to show when an error occurs.|Uri|  
  
## Remarks  
 The deployment manifest file identifies a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application deployment, including the current version and other deployment settings. It references the application manifest, which describes the current version of the application and all of the files contained within the deployment.  
  
 For more information, see [ClickOnce Deployment Overview](../Topic/ClickOnce%20Security%20and%20Deployment.md).  
  
## File Location  
 The deployment manifest file references the correct application manifest for the current version of the application. When you make a new version of an application deployment available, you must update the deployment manifest to refer to the new application manifest.  
  
 The deployment manifest file must be strongly named and can also contain certificates for publisher validation.  
  
## File Name Syntax  
 The name of a deployment manifest file must end with the .application extension.  
  
## Examples  
 The following code example illustrates a deployment manifest.  
  
```  
<?xml version="1.0" encoding="utf-8"?>  
<asmv1:assembly xsi:schemaLocation="urn:schemas-microsoft-com:asm.v1 assembly.adaptive.xsd"  
  manifestVersion="1.0"  
  xmlns:asmv3="urn:schemas-microsoft-com:asm.v3"  
  xmlns:dsig=http://www.w3.org/2000/09/xmldsig#  
  xmlns:co.v1="urn:schemas-microsoft-com:clickonce.v1"  
  xmlns:co.v2="urn:schemas-microsoft-com:clickonce.v2"  
  xmlns="urn:schemas-microsoft-com:asm.v2"  
  xmlns:asmv1="urn:schemas-microsoft-com:asm.v1"  
  xmlns:asmv2="urn:schemas-microsoft-com:asm.v2"  
  xmlns:xrml="urn:mpeg:mpeg21:2003:01-REL-R-NS"  
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">  
  <assemblyIdentity   
    name="My Application Deployment.app"  
    version="1.0.0.0"  
    publicKeyToken="43cb1e8e7a352766"  
    language="neutral"  
    processorArchitecture="x86"  
    xmlns="urn:schemas-microsoft-com:asm.v1" />  
  <description  
    asmv2:publisher="My Company Name"  
    asmv2:product="My Application"  
    xmlns="urn:schemas-microsoft-com:asm.v1" />  
  <deployment install="true">  
    <subscription>  
      <update>  
        <expiration maximumAge="0" unit="days" />  
      </update>  
    </subscription>  
    <deploymentProvider codebase="\\myServer\sampleDeployment\MyApplicationDeployment.application" />  
  </deployment>  
  <compatibleFrameworks xmlns="urn:schemas-microsoft-com:clickonce.v2">  
    <framework targetVersion="4.0" profile="Full" supportedRuntime="4.0.20506" />  
    <framework targetVersion="4.0" profile="Client" supportedRuntime="4.0.20506" />  
  </compatibleFrameworks>  
  <dependency>  
    <dependentAssembly  
      dependencyType="install"  
      codebase="1.0.0.0\My Application Deployment.exe.manifest"  
      size="6756">  
      <assemblyIdentity  
        name="My Application Deployment.exe"  
        version="1.0.0.0"  
        publicKeyToken="43cb1e8e7a352766"  
        language="neutral"  
        processorArchitecture="x86"  
        type="win32" />  
      <hash>  
        <dsig:Transforms>  
          <dsig:Transform Algorithm="urn:schemas-microsoft-com:HashTransforms.Identity" />  
        </dsig:Transforms>  
        <dsig:DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1" />  
        <dsig:DigestValue>E506x9FwNauks7UjQywmzgtd3FE=</dsig:DigestValue>  
      </hash>  
    </dependentAssembly>  
  </dependency>  
<publisherIdentity name="CN=DOMAIN\MyUsername" issuerKeyHash="18312a18a21b215ecf4cdb20f5a0e0b0dd263c08" /><Signature Id="StrongNameSignature" xmlns="http://www.w3.org/2000/09/xmldsig#">  
…  
</Signature></asmv1:assembly>  
```  
  
## See Also  
 [Publishing ClickOnce Applications](../vs140/Publishing-ClickOnce-Applications.md)