---
title: "operator&lt;= (&lt;forward_list&gt;)"
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
ms.assetid: 0d0acb70-2258-4247-bb21-d176b1e31488
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&lt;= (&lt;forward_list&gt;)
Tests if the forward list object on the left side of the operator is less than or equal to the forward list object on the right side.  
  
## Syntax  
  
```  
bool operator<=(  
    const forward_list <Type, Allocator>& _Left,  
    const forward_list <Type, Allocator>& _Right  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Left`|An object of type `forward_list`.|  
|`_Right`|An object of type `forward_list`.|  
  
## Return Value  
 `true` if the list on the left side of the operator is less than or equal to the list on the right side of the operator; otherwise `false`.  
  
## Remarks  
 This template function returns `!(_Right < _Left)`.  
  
## Requirements  
 **Header:** <forward_list>  
  
 **Namespace:** std  
  
## See Also  
 [<forward_list>](../vs140/-forward_list-.md)