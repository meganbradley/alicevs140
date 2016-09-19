---
title: "How to: Create a .Vsct File from an Existing .Cto File"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 847717c9-477d-4ac9-8b2c-2da878912478
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a .Vsct File from an Existing .Cto File
You can create an XML-based .vsct file from an existing binary .cto file. Doing this allows you to take advantage of the new command table compiler format. This process works even if the .cto file was compiled from a .ctc file. You can edit and compile the .vsct file into another .cto file.  
  
### To create a .vsct file from a .cto file  
  
1.  Obtain copies of the .cto file and its corresponding .ctsym file.  
  
2.  Place the files into the same directory as the vsct.exe compiler.  
  
3.  At the Visual Studio Command Prompt, go to the directory that contains the .cto and .ctsym files.  
  
4.  Type **vsct.exe** *ctofilename***.cto** *vsctfilename***.vsct -S***symfilename***.ctsym**.  
  
     `ctofilename` is the name of the .cto file, `vsctfilename` is the name of the vsct file you want to create, and `symfilename` is the name of the .ctsym file.  
  
     This process creates a new .vsct XML command table compiler file. You can edit and compile the file with vsct.exe, the vsct compiler, as you would any other .vsct file.  
  
## See Also  
 [How To: Create a New .vsct File](../vs140/How-to--Create-a-.Vsct-File.md)   
 [XML-Based Command Table Configuration (.vsct) Files](../vs140/Visual-Studio-Command-Table--.Vsct--Files.md)