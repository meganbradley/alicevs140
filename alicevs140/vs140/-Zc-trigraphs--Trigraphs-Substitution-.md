---
title: "-Zc:trigraphs (Trigraphs Substitution)"
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
H1: /Zc:trigraphs (Trigraphs Substitution)
ms.assetid: e3d6058f-400d-4966-a3aa-800cfdf69cbf
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Zc:trigraphs (Trigraphs Substitution)
When **/Zc:trigraphs** is specified, the compiler replaces a trigraph character sequence by using a corresponding punctuation character. To turn off trigraph substitution, specify **/Zc:trigraphs-**. By default, **/Zc:trigraphs** is off.  
  
## Syntax  
  
```  
/Zc:trigraphs[-]  
```  
  
## Remarks  
 A trigraph consists of two consecutive question marks ("??") followed by a unique third character. For example, the compiler replaces the "??=" trigraph by using the '#' character. Use trigraphs in C source files that use a character set that does not contain convenient graphic representations for some punctuation characters.  
  
 For a list of C/C++ trigraphs, and an example that shows how to use trigraphs, see [Trigraphs](../vs140/Trigraphs.md).  
  
## See Also  
 [/Zc (Conformance)](../vs140/-Zc--Conformance-.md)   
 [Trigraphs](../vs140/Trigraphs.md)