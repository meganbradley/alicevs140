---
title: "Compiler Warning (level 1) CS1697"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0cd931b7-f358-4ff0-b441-27668645d7d5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1697
Different checksum values given for 'file name'  
  
 You have specified more than one checksum for a given file. The debugger uses the checksum value to determine which file to debug when there is more than one file in a project with the same name. Most users will not encounter this error, but if you are writing an application that generates code, you may run into it. To resolve this error, ensure that you generate the checksum only once for any given code file.