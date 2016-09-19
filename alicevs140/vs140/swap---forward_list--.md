---
title: "swap (&lt;forward_list&gt;)"
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
ms.assetid: 78ccb4f7-3f26-43f2-a7cc-85fe034aa969
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# swap (&lt;forward_list&gt;)
Exchanges the elements of two forward lists.  
  
## Syntax  
  
```  
void swap(  
    forward_list <Type, Allocator>& _Left,  
    forward_list <Type, Allocator>& _Right  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Left`|An object of type `forward_list`.|  
|`_Right`|An object of type `forward_list`.|  
  
## Remarks  
 This template function executes `_Left.swap(_Right)`.  
  
## Requirements  
 **Header:** <forward_list>  
  
 **Namespace:** std  
  
## See Also  
 [<forward_list>](../vs140/-forward_list-.md)