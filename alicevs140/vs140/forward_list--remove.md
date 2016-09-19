---
title: "forward_list::remove"
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
ms.assetid: 73af57b5-b75c-4ead-a424-3391b080b628
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# forward_list::remove
Erases elements in a forward list that matches a specified value.  
  
## Syntax  
  
```  
void remove(const Type& _Val);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Val`|The value which, if held by an element, will result in that element's removal from the list.|  
  
## Remarks  
 The member function removes from the controlled sequence all elements, designated by the iterator `P`, for which `*P == _Val`.  
  
 The member function never throws an exception.  
  
## Requirements  
 **Header:** <forward_list>  
  
 **Namespace:** std  
  
## See Also  
 [forward_list Class](../vs140/forward_list-Class.md)