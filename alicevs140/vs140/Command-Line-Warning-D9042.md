---
title: "Command-Line Warning D9042"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d710693b-e422-40b2-b2dd-79e1b163b9e6
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Command-Line Warning D9042
invalid value 'value' for '/option'; assuming 'value'; Code Analysis warnings are not available in this edition of the compiler  
  
 A Code Analysis warning number was added to the **/wd**, **/we**, **/wo**, or **/wl** command line option and the **/analyze** command line option was specified on a platform that does not support Code Analysis. To remedy this warning, either switch to the x86 version of Visual Studio Team System, or remove the **/analyze** command line option.  
  
## Example  
 The following command line example generates the warning D9042 on an x64 or Itanium system:  
  
```  
cl /EHsc /LD /wd6001 /analyze filename.cpp  
```  
  
 To remedy this warning, either switch to the x86 version of Visual Studio Team System, or remove the **/analyze** and **/wd6001** command line options.  
  
## See Also  
 [Command-Line Errors D8000 Through D9999](../vs140/Command-Line-Errors-D8000-Through-D9999.md)   
 [Compiler Options](../vs140/Compiler-Options.md)