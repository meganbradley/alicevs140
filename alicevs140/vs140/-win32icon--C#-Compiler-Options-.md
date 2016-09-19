---
title: "-win32icon (C# Compiler Options)"
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
H1: /win32icon (C# Compiler Options)
ms.assetid: 756d9b6d-ab07-41b7-ba58-5bd88f711138
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -win32icon (C# Compiler Options)
The **/win32icon** option inserts an .ico file in the output file, which gives the output file the desired appearance in the File Explorer.  
  
## Syntax  
  
```  
/win32icon:filename  
```  
  
## Arguments  
 `filename`  
 The .ico file that you want to add to your output file.  
  
## Remarks  
 An .ico file can be created with the [Resource Compiler](http://go.microsoft.com/fwlink/?LinkId=148370). The Resource Compiler is invoked when you compile a Visual C++ program; an .ico file is created from the .rc file.  
  
 See [/linkresource](../Topic/-linkresource%20\(C%23%20Compiler%20Options\).md) (to reference) or [/resource](../Topic/-resource%20\(C%23%20Compiler%20Options\).md) (to attach) a .NET Framework resource file. See [/win32res](../vs140/-win32res--C#-Compiler-Options-.md) to import a .res file.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Properties** pages.  
  
2.  Click the **Application** property page.  
  
3.  Modify the **Application icon** property.  
  
 For information on how to set this compiler option programmatically, see <xref:VSLangProj80.ProjectProperties3.ApplicationIcon?qualifyHint=False>.  
  
## Example  
 Compile `in.cs` and attach an .ico file `rf.ico` to produce `in.exe`:  
  
```  
csc /win32icon:rf.ico in.cs  
```  
  
## See Also  
 [C# Compiler Options](../vs140/C#-Compiler-Options.md)   
 [NIB How to: Modify Project Properties and Configuration Settings](assetId:///e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)