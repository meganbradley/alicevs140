---
title: "Compiler Warning (level 4) C4152"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6025ab70-d7cf-4730-913a-3ca0b1186a3a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4152
non standard extension, function/data ptr conversion in expression  
  
 A function pointer is converted to or from a data pointer. This conversion is allowed under Microsoft extensions (/Ze) but not under ANSI C.