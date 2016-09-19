---
title: "Compiler Error C2002"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 91982314-203a-4de1-b884-94e39a623f61
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2002
invalid wide-character constant  
  
 The multibyte-character constant is not valid.  
  
### To fix by checking the following possible causes  
  
1.  The wide-character constant contains more bytes than expected.  
  
2.  The standard header STDDEF.h is not included.  
  
3.  Wide characters cannot be concatenated with ordinary string literals.  
  
4.  A wide-character constant must be preceded by the character 'L':  
  
    ```  
    L'mbconst'  
    ```  
  
5.  For Microsoft C++, the text arguments of a preprocessor directive must be ASCII. For example, the directive, `#pragma message(L"string")`, is not valid.