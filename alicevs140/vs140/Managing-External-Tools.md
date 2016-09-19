---
title: "Managing External Tools"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f382fd40-a98f-4934-8c9a-5aeae881acde
caps.latest.revision: 40
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Managing External Tools
You can call external tools from inside Visual Studio. A few default tools are available from the **Tools** menu, but you can add other executables of your own.  
  
## Tools Available on the Visual Studio Tools Menu  
 You can call the following tools from the **Tools** menu in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. You can also call them by name from the **Quick Launch** window. For example, to call GuidGen.exe, type **Create GUID**.  
  
1.  Create GUID: generates a GUID.  
  
2.  Error Lookup: gets an error message from the value entered. For more information, see [ERRLOOK Reference](../vs140/ERRLOOK-Reference.md).  
  
3.  ATL/MFC Trace Tool: shows debug trace messages in the ATL and MFC sources.  
  
4.  PreEmptive Dotfuscator and Analytics: Protects .NET programs against reverse engineering.  
  
5.  SPY++: Displays processes, threads, windows, and window messages graphically.  
  
6.  WCF Service Configuration Editor: Allows you to create and modify configuration settings for WCF services.  
  
> [!WARNING]
>  You may see a different list of external tools, depending on which Visual Studio edition you have installed and the settings profile you have applied. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
## Adding New Tools  
 You can add an external tool to the **Tools** menu. Open the **External Tools** dialog box and click **Add**, then fill in the information. For example, the following entry causes Windows Explorer to open at the directory of the file you currently have open in Visual Studio:  
  
1.  Title: Open File Location  
  
2.  Command: explorer.exe  
  
3.  Arguments: /root, "$(ItemDir)"  
  
## Arguments for external tools  
 The following arguments are Visual Studio variables that are assigned when you launch an external tool. Links to external tools such as Notepad or Spy++ can be listed on the **Tools** menu using the External Tools dialog box.  
  
> [!NOTE]
>  The IDE status bar displays the Current Line and Current Column variables to indicate where the insertion point is located in the active Code Editor. The Current Text variable returns the text or code selected at that location.  
  
|Name|Argument|Description|  
|----------|--------------|-----------------|  
|Item Path|$(ItemPath)|The complete file name of the current file (drive + path + file name).|  
|Item Directory|$(ItemDir)|The directory of the current file (drive + path).|  
|Item File Name|$(ItemFilename)|The file name of the current file (file name).|  
|Item Extension|$(ItemExt)|The file name extension of the current file.|  
|Current Line|$(CurLine)|The current line position of the cursor in the code window.|  
|Current Column|$(CurCol)|The current column position of the cursor in the code window.|  
|Current Text|$(CurText)|The selected text.|  
|Target Path|$(TargetPath)|The complete file name of the item to be built (drive + path + file name).|  
|Target Directory|$(TargetDir)|The directory of the item to be built.|  
|Target Name|$(TargetName)|The file name of the item to be built.|  
|Target Extension|$(TargetExt)|The file name extension of the item to be built.|  
|Binary Directory|$(BinDir)|The final location of the binary that is being built (defined as drive + path). For example:**\\...\My Documents\Visual Studio <Version\>\\<ProjectName\>\bin\debug**|  
|Project Directory|$(ProjDir)|The directory of the current project (drive + path).|  
|Project file name|$(ProjFileName)|The file name of the current project (drive + path + file name).|  
|Solution Directory|$(SolutionDir)|The directory of the current solution (drive + path).|  
|Solution file name|$(SolutionFileName)|The file name of the current solution (drive + path + file name).|  
  
## See Also  
 [C/C++ Build Tools](../vs140/C-C---Build-Tools.md)