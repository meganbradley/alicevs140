---
title: "-ENTRY (Entry-Point Symbol)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: /ENTRY (Entry-Point Symbol)
ms.assetid: 26c62ba2-4f52-4882-a7bd-7046a0abf445
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -ENTRY (Entry-Point Symbol)
```  
/ENTRY:function  
```  
  
## Remarks  
 where:  
  
 *function*  
 A function that specifies a user-defined starting address for an .exe file or DLL.  
  
## Remarks  
 The /ENTRY option specifies an entry point function as the starting address for an .exe file or DLL.  
  
 The function must be defined with the `__stdcall` calling convention. The parameters and return value depend on if the program is a console application, a windows application or a DLL. It is recommended that you let the linker set the entry point so that the C run-time library is initialized correctly, and C++ constructors for static objects are executed.  
  
 By default, the starting address is a function name from the C run-time library. The linker selects it according to the attributes of the program, as shown in the following table.  
  
|Function name|Default for|  
|-------------------|-----------------|  
|**mainCRTStartup** (or **wmainCRTStartup**)|An application using /SUBSYSTEM:**CONSOLE**; calls **main** (or **wmain**)|  
|**WinMainCRTStartup** (or **wWinMainCRTStartup**)|An application using /SUBSYSTEM:**WINDOWS**; calls `WinMain` (or **wWinMain**), which must be defined with `__stdcall`|  
|**_DllMainCRTStartup**|A DLL; calls `DllMain`, which must be defined with `__stdcall`, if it exists|  
  
 If the [/DLL](../vs140/-DLL--Build-a-DLL-.md) or [/SUBSYSTEM](../Topic/-SUBSYSTEM%20\(Specify%20Subsystem\).md) option is not specified, the linker selects a subsystem and entry point depending on whether **main** or `WinMain` is defined.  
  
 The functions **main**, `WinMain`, and `DllMain` are the three forms of the user-defined entry point.  
  
 When creating a managed image, the function specified with /ENTRY must have a signature of (LPVOID *var1*, DWORD *var2*, LPVOID *var3*).  
  
 For information on how to define your own DllMain entry point, see [Run-Time Library Behavior](../vs140/Run-Time-Library-Behavior.md) .  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **Advanced** property page.  
  
4.  Modify the **Entry Point** property.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.EntryPointSymbol?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)