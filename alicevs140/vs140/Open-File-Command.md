---
title: "Open File Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a51a83fc-e3c6-4fa2-8882-8b7b6c0a6406
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Open File Command
Opens an existing file and allows you to specify an editor.  
  
## Syntax  
  
```  
File.OpenFile filename [/e:editorname]  
```  
  
## Arguments  
 `filename`  
 Required. The full or partial path and file name of the file to open. Paths containing spaces must be enclosed in quotation marks.  
  
## Switches  
 /e:`editorname`  
 Optional. Name of the editor in which the file will be opened. If the argument is specified but no editor name is supplied, the **Open With** dialog box appears.  
  
 The /e:`editorname` argument syntax uses the editor names as they appear in the Open With Dialog Box, enclosed in quotation marks.  
  
 For example, to open a file in the source code editor, you would enter the following for the /e:`editorname` argument.  
  
```  
/e:"Source Code (text) Editor"  
```  
  
## Remarks  
 As you enter a path, auto completion tries to locate the correct path and file name.  
  
## Example  
 This example opens the style file "Test1.css" in the source code editor.  
  
```  
>File.OpenFile "C:\My Projects\project1\Test1.css" /e:"Source Code (text) Editor"  
```  
  
## See Also  
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Immediate Window](../vs140/Immediate-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)