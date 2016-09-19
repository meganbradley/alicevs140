---
title: "forward_list::emplace_front"
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
ms.assetid: cacd3a62-8949-4b90-b688-eccca84f912a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# forward_list::emplace_front
Adds an element constructed in place to the beginning of the list.  
  
## Syntax  
  
```  
template<class Type>  
    void emplace_front(Type&& _Val);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Val`|The element added to the beginning of the forward list.|  
  
## Remarks  
 This member function inserts an element with the constructor arguments `__Val` at the end of the controlled sequence.  
  
 If an exception is thrown, the container is left unaltered and the exception is rethrown.  
  
## Requirements  
 **Header:** <forward_list>  
  
 **Namespace:** std  
  
## See Also  
 [forward_list Class](../vs140/forward_list-Class.md)