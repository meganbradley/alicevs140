---
title: "GetWinFXPath Task"
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
ms.assetid: b1dfb467-f3d3-47f3-83ef-af7b0e33a772
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetWinFXPath Task
The <xref:Microsoft.Build.Tasks.Windows.GetWinFXPath?qualifyHint=False> task returns the directory of the current [!INCLUDE[TLA#tla_winfx](../vs140/includes/TLA#tla_winfx_md.md)] runtime.  
  
## Task Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`WinFXPath`|Optional **String** output parameter.<br /><br /> Specifies the real path to the [!INCLUDE[TLA2#tla_winfx](../vs140/includes/TLA2#tla_winfx_md.md)] runtime.|  
|`WinFXNativePath`|Required **String** parameter.<br /><br /> Specifies the path to the native [!INCLUDE[TLA2#tla_titlewinfx](../vs140/includes/TLA2#tla_titlewinfx_md.md)] runtime.|  
|`WinFXWowPath`|Required **String** parameter.<br /><br /> Specifies the path to the [!INCLUDE[TLA#tla_winfx](../vs140/includes/TLA#tla_winfx_md.md)] assemblies in the 32-bit **Windows on Windows** module on 64-bit systems.|  
  
## Remarks  
 If the <xref:Microsoft.Build.Tasks.Windows.GetWinFXPath?qualifyHint=False> task is executing on a 64-bit processor, the **WinFXPath** parameter is set to the path that is stored in the **WinFXWowPath** parameter; otherwise, the **WinFXPath** parameter is set to the path that is stored in the **WinFXNativePath** parameter.  
  
## Example  
 The following example shows how to use the **GetWinFXPath** task to detect the native path to the [!INCLUDE[TLA2#tla_titlewinfx](../vs140/includes/TLA2#tla_titlewinfx_md.md)] runtime.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  <UsingTask   
    TaskName="Microsoft.Build.Tasks.Windows.GetWinFXPath"   
    AssemblyFile="C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationBuildTasks.dll" />  
  <Target Name="GetWinFXPathTask">  
    <GetWinFXPath  
      WinFXNativePath="c:\WinFXNative"   
      WinFXWowPath="c:\WinFXWowNative" />  
  </Target>  
  <Import Project="$(MSBuildBinPath)\Microsoft.WinFX.targets" />  
</Project>  
```  
  
## See Also  
 [WPF MSBuild Reference](../Topic/WPF%20MSBuild%20Reference.md)   
 [WPF MSBuild Task Reference](../vs140/WPF-MSBuild-Task-Reference.md)   
 [MSBuild Reference](../Topic/MSBuild%20Reference.md)   
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)   
 [Building a WPF Application (WPF)](assetId:///a58696fd-bdad-4b55-9759-136dfdf8b91c)