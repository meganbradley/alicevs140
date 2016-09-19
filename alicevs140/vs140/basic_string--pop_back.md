---
title: "basic_string::pop_back"
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
ms.assetid: 87e522c2-c10d-4900-a944-86ab7884ab27
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_string::pop_back
Erases the last element of the string.  
  
## Syntax  
  
```  
void pop_back();  
```  
  
## Remarks  
 This member function effectively calls `erase(size() - 1)` to erase the last element of the sequence, which must be non-empty.  
  
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_string Class](../vs140/basic_string-Class.md)   
 [<string\>](../vs140/-string-.md)