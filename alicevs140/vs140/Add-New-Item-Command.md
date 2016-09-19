---
title: "Add New Item Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 63b7df32-db83-463b-bbe7-7ff011fe5298
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Add New Item Command
Adds a new solution item, such as an .htm, .css, .txt, or frameset to the current solution and opens it.  
  
## Syntax  
  
```  
File.AddNewItem [filename] [/t:templatename] [/e:editorname]  
```  
  
## Arguments  
 `filename`  
 Optional. The path and file name of the item to add to the solution.  
  
## Switches  
 /t: `templatename`  
 Optional. Specifies the type of file to be created. If no template name is given, a text file is created by default.  
  
 The /t:`templatename` argument syntax mirrors the information found in the **Add New Solution Item** dialog box. You must enter the complete category followed by the file type, separating the category name from the file type by a backslash (`\`) and enclosing the entire string in quotation marks.  
  
 For example, to create a new text file, you would enter the following for the /t:`templatename` argument.  
  
```  
/t:"General\Style Sheet"  
```  
  
 /e: `editorname`  
 Optional. The name of the editor in which the file will be opened. If the argument is specified but no editor name is supplied, the **Open With** dialog box appears.  
  
 The /e:`editorname` argument syntax uses the editor names as they appear in the **Open With Dialog Box**, enclosed in quotation marks.  
  
 For example, to open a style sheet in the source code editor, you would enter the following for the /e:`editorname` argument.  
  
```  
/e:"Source Code (text) Editor"  
```  
  
## Example  
 This example adds a new solution item, MyHTMLpg, to the current solution.  
  
```  
>File.AddNewItem MyHTMLpg /t:"General\HTML Page"  
```  
  
## See Also  
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)