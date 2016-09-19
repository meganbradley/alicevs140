---
title: "Open Project Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: baa85f86-041b-49f4-9ced-0c397dc180e1
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Open Project Command
Opens an existing project.  
  
## Syntax  
  
```  
File.OpenProject filename  
```  
  
## Arguments  
 `filename`  
 Required. The full path and file name of the project to open.  
  
 The syntax for the `filename` argument requires that paths containing spaces use quotation marks.  
  
## Remarks  
 Auto completion tries to locate the correct path and file name as you type.  
  
 This command is not available while debugging.  
  
## Example  
 This example opens the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] project, Test1.  
  
```  
>File.OpenProject "C:\My Projects\Test1\Test1.vbproj"  
```  
  
## See Also  
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)