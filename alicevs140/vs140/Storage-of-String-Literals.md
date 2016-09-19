---
title: "Storage of String Literals"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba5e4d2c-d456-44b3-a8ca-354af547ac50
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Storage of String Literals
The characters of a literal string are stored in order at contiguous memory locations. An escape sequence (such as **\\\\** or **\\"**) within a string literal counts as a single character. A null character (represented by the **\0** escape sequence) is automatically appended to, and marks the end of, each string literal. (This occurs during [translation phase](../vs140/Phases-of-Translation.md) 7.) Note that the compiler may not store two identical strings at two different addresses. [/GF](../Topic/-GF%20\(Eliminate%20Duplicate%20Strings\).md) forces the compiler to place a single copy of identical strings into the executable file.  
  
## Remarks  
 **Microsoft Specific**  
  
 Strings have static storage duration. See [Storage Classes](../vs140/C-Storage-Classes.md) for information about storage duration.  
  
 **END Microsoft Specific**  
  
## See Also  
 [C String Literals](../vs140/C-String-Literals.md)