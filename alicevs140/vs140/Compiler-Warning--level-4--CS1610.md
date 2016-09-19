---
title: "Compiler Warning (level 4) CS1610"
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
ms.topic: error-reference
ms.assetid: dc78dbcc-d5a0-4776-953c-1fe72b6fd5ea
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) CS1610
Unable to delete temporary file 'file' used for default Win32 resource -- resource  
  
 When using the [/win32res](../vs140/-win32res--C#-Compiler-Options-.md) compiler option and when your **%TEMP%** directory does not have DELETE permission, this warning indicates that the compiler could not delete a temporary file that it created.  
  
 Make sure that you have read/write/delete permissions for the **%TEMP%** directory.  
  
 If necessary, you can manually delete these files and there will be no harm to C# or any of your programs.