---
title: "operator!= (&lt;allocators&gt;)"
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
ms.assetid: b33c8fae-4866-4cef-a462-491b423cf71d
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# operator!= (&lt;allocators&gt;)
Tests for inequality between allocator objects of a specified class.  
  
## Syntax  
  
```  
template <class Type, class Sync>  
    bool operator!=(  
        const allocator_base<Type, Sync>& _Left,  
        const allocator_base<Type, Sync>& _Right  
    );  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Left`|One of the allocator objects to be tested for inequality.|  
|`_Right`|One of the allocator objects to be tested for inequality.|  
  
## Return Value  
 **true** if the allocator objects are not equal; **false** if allocator objects are equal.  
  
## Remarks  
 The template operator returns `!(_Left == _Right)`.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [<allocators\>](../vs140/-allocators-.md)