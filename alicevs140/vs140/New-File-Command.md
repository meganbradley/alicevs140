---
title: "New File Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 767868d6-a525-425b-a43b-2198f636ab6b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# New File Command
Creates a new file and opens it. The file appears under the Miscellaneous Files folder.  
  
## Syntax  
  
```  
File.NewFile [filename] [/t:templatename] [/editor:editorname]  
```  
  
## Arguments  
 `filename`  
 Optional. Name for the file. If no name is supplied, a default name is provided. If no template name is listed, a text file is created.  
  
## Switches  
 /t:`templatename`  
 Optional. Specifies the type of file to be created.  
  
 The /t:`templatename` argument syntax mirrors the information found in the New File Dialog Box. Enter the category name followed by a backslash (`\`) and the template name, and enclose the entire string in quotation marks.  
  
 For example, to create a new [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] source file, you would enter the following for the /t:`templatename` argument.  
  
```  
/t:"Visual C++\C++ File (.cpp)"  
```  
  
 The example above indicates that the C++ File template is located under the Visual C++ category in the **New File** dialog box.  
  
 /e:`editorname`  
 Optional. Name of the editor in which the file will be opened. If the argument is specified but no editor name is supplied, the **Open With** dialog box appears.  
  
 The /e:`editorname` argument syntax uses the editor names as they appear in the Open With Dialog Box, enclosed in quotation marks.  
  
 For example, to open a file in the source code editor, you would enter the following for the /e:`editorname` argument.  
  
```  
/e:"Source Code (text) Editor"  
```  
  
## Example  
 This example creates a new Web page "test1.htm" and opens it in the source code editor.  
  
```  
>File.NewFile test1 /t:"General\HTML Page" /e:"Source Code (text) Editor"  
```  
  
## See Also  
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Immediate Window](../vs140/Immediate-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)