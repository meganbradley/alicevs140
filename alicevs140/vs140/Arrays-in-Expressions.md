---
title: "Arrays in Expressions"
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
ms.topic: language-reference
ms.assetid: 6e5a795b-d6bd-4e39-b313-6a20d47c4d4b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Arrays in Expressions
When an identifier of an array type appears in an expression other than `sizeof`, address-of (**&**), or initialization of a reference, it is converted to a pointer to the first array element. For example:  
  
```  
char szError1[] = "Error: Disk drive not ready.";  
char *psz = szError1;  
```  
  
 The pointer `psz` points to the first element of the array `szError1`. Note that arrays, unlike pointers, are not modifiable l-values. Therefore, the following assignment is illegal:  
  
```  
szError1 = psz;  
```  
  
## See Also  
 [Arrays](../vs140/Arrays--C---.md)