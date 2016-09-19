---
title: "Compiler Error CS1567"
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
ms.assetid: 837b9855-191b-4384-ad45-52960906679c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1567
Error generating Win32 resource: 'file'  
  
 Your compilation either used the [/win32icon](../vs140/-win32icon--C#-Compiler-Options-.md) compiler option or did not use [/win32res](../vs140/-win32res--C#-Compiler-Options-.md), which causes the compiler to generate a file that contains resource information, but the compiler was unable to create the file due to insufficient disk space or some other error.  
  
 If you are unable to resolve the file-generation problem, you could use [/win32res](../vs140/-win32res--C#-Compiler-Options-.md), which does not generate a file that contains resource information.