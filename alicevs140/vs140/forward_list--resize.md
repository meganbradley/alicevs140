---
title: "forward_list::resize"
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
ms.assetid: 56ddc483-1734-4621-b3bf-4483b2f0556c
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# forward_list::resize
Specifies a new size for a forward list.  
  
## Syntax  
  
```  
void resize(size_type _Newsize);  
void resize(size_type _Newsize, const Type& _Val);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Newsize`|The number of elements in the resized forward list.|  
|`_Val`|The value to use for padding.|  
  
## Remarks  
 The member functions both ensure that the number of elements in the list henceforth is `_Newsize`. If it must make the controlled sequence longer, the first member function appends elements with value `Type()`, while the second member function appends elements with value `_Val`. To make the controlled sequence shorter, both member functions effectively call `erase_after(begin() + _Newsize - 1, end())`.  
  
## Requirements  
 **Header:** <forward_list>  
  
 **Namespace:** std  
  
## See Also  
 [forward_list Class](../vs140/forward_list-Class.md)