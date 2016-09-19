---
title: "-codepage (C# Compiler Options)"
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
H1: /codepage (C# Compiler Options)
ms.assetid: 75942989-b69a-4308-90a0-840c73d2c478
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -codepage (C# Compiler Options)
This option specifies which codepage to use during compilation if the required page is not the current default codepage for the system.  
  
## Syntax  
  
```  
/codepage:id  
```  
  
## Arguments  
 `id`  
 The id of the code page to use for all source code files in the compilation.  
  
## Remarks  
 If you compile one or more source code files that were not created to use the default code page on your computer, you can use the **/codepage** option to specify which code page should be used. **/codepage** applies to all source code files in your compilation.  
  
 If the source code files were created with the same codepage that is in effect on your computer or if the source code files were created with UNICODE or UTF-8, you need not use **/codepage**.  
  
 See [GetCPInfo](http://go.microsoft.com/fwlink/?LinkId=148371) for information on how to find which code pages are supported on your system.  
  
 This compiler option is unavailable in Visual Studio and cannot be changed programmatically.  
  
## See Also  
 [C# Compiler Options](../vs140/C#-Compiler-Options.md)   
 [NIB How to: Modify Project Properties and Configuration Settings](assetId:///e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)