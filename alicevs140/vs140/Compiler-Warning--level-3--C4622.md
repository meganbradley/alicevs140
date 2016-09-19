---
title: "Compiler Warning (level 3) C4622"
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
ms.assetid: d3c879f0-4492-4f4b-b26d-230993f3a933
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4622
Overwriting debug information formed during creation of the precompiled header in object file: 'file'  
  
 CodeView information in the specified file was lost when it was compiled with the [/Yu](../vs140/-Yu--Use-Precompiled-Header-File-.md) (Use Precompiled Headers) option.  
  
 Rename the object file (using [/Fo](../Topic/-Fo%20\(Object%20File%20Name\).md)) when creating or using the precompiled header file, and link using the new object file.