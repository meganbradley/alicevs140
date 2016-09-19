---
title: "Creating an .Sbr File"
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
ms.assetid: bdb4b93c-a88a-441a-84fd-01087d03be25
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating an .Sbr File
The input files for BSCMAKE are .sbr files. The compiler creates an .sbr file for each object file (.obj) it compiles. When you build or update your browse information file, all .sbr files for your project must be available on disk.  
  
 To create an .sbr file with all possible information, specify [/FR](../vs140/-FR---Fr--Create-.Sbr-File-.md).  
  
 To create an .sbr file that doesn't contain local symbols, specify [/Fr](../vs140/-FR---Fr--Create-.Sbr-File-.md). If the .sbr files contain local symbols, you can still omit them from the .bsc file by using BSCMAKE's [/El option](../vs140/BSCMAKE-Options.md)`.`  
  
 You can create an .sbr file without performing a full compile. For example, you can specify the /Zs option to the compiler to perform a syntax check and still generate an .sbr file if you specify /FR or /Fr.  
  
 The build process can be more efficient if the .sbr files are first packed to remove unreferenced definitions. The compiler automatically packs .sbr files.  
  
## See Also  
 [Building a .Bsc File](../vs140/Building-a-.Bsc-File.md)