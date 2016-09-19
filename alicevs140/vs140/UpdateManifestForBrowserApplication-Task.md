---
title: "UpdateManifestForBrowserApplication Task"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - jsharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 653339f7-654b-4d64-a26a-5c9f27036895
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# UpdateManifestForBrowserApplication Task
The <xref:Microsoft.Build.Tasks.Windows.UpdateManifestForBrowserApplication?qualifyHint=False> task is run to add the **<hostInBrowser /\>** element to the application manifest (*projectname*.exe.manifest) when a [!INCLUDE[TLA#tla_xbap](../vs140/includes/TLA#tla_xbap_md.md)] project is built.  
  
## Task Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`ApplicationManifest`|Required **ITaskItem[]** parameter.<br /><br /> Specifies the path and name of the application manifest file that you want to add the `<hostInBrowser />` element to.|  
|`HostInBrowser`|Required **Boolean** parameter.<br /><br /> Specifies whether to modify the application manifest to include the **<hostInBrowser /\>** element. If **true**, a new `<`**hostInBrowser />** element is included in the **<entryPoint /\>** element. Note that element inclusion is cumulative: if a **<hostInBrowser /\>** element already exists, it is not removed or overwritten. Instead, an additional **<hostInBrowser /\>** element is created. If **false**, the application manifest is not modified.|  
  
## Remarks  
 [!INCLUDE[TLA2#tla_xbap#plural](../vs140/includes/TLA2#tla_xbap#plural_md.md)] are run by using [!INCLUDE[TLA#tla_clickonce](../vs140/includes/TLA#tla_clickonce_md.md)] deployment and, therefore, must by published with supporting deployment and application manifests. [!INCLUDE[TLA#tla_msbuild](../vs140/includes/TLA#tla_msbuild_md.md)] uses the [GenerateApplicationManifest](http://msdn2.microsoft.com/library/6wc2ccdc.aspx) task to generate an application manifest.  
  
 Then, to configure an application to be hosted from a browser, an additional element, **<hostInBrowser /\>** must be added to the application manifest, as show in the following example:  
  
```  
<!--MyXBAPApplication.exe.manifest-->  
<?xml version="1.0" encoding="utf-8"?>  
<asmv1:assembly ... >  
    <asmv1:assemblyIdentity ... />  
    <application />  
    <entryPoint>  
      ...  
      <hostInBrowser xmlns="urn:schemas-microsoft-com:asm.v3" />  
    </entryPoint>  
  ...  
/>  
```  
  
 The <xref:Microsoft.Build.Tasks.Windows.UpdateManifestForBrowserApplication?qualifyHint=False> task is run when an [!INCLUDE[TLA2#tla_xbap](../vs140/includes/TLA2#tla_xbap_md.md)] project is built in order to add the `<hostInBrowser />` element.  
  
## Example  
 The following example shows how to ensure that the `<hostInBrowser />` element is included in an application manifest file.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  <UsingTask   
    TaskName="Microsoft.Build.Tasks.Windows.UpdateManifestForBrowserApplication"  
    AssemblyFile="C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationBuildTasks.dll" />  
  <Target Name="UpdateManifestForBrowserApplicationTask">  
    <UpdateManifestForBrowserApplication  
      ApplicationManifest="MyXBAPApplication.exe.manifest"  
      HostInBrowser="true" />  
  </Target>  
</Project>  
```  
  
## See Also  
 [WPF MSBuild Reference](../Topic/WPF%20MSBuild%20Reference.md)   
 [WPF MSBuild Task Reference](../vs140/WPF-MSBuild-Task-Reference.md)   
 [MSBuild Reference](../Topic/MSBuild%20Reference.md)   
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)   
 [Building a WPF Application (WPF)](assetId:///a58696fd-bdad-4b55-9759-136dfdf8b91c)   
 [WPF XAML Browser Applications Overview](assetId:///3a7a86a8-75d5-4898-96b9-73da151e5e16)