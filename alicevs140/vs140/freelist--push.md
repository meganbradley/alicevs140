---
title: "freelist::push"
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
ms.assetid: 80c9b920-48e7-497b-a2da-85bdf76d4741
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# freelist::push
Adds a memory block to the list.  
  
## Syntax  
  
```  
bool push(void* _Ptr);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Ptr`|A pointer to the memory block to be added to the free list.|  
  
## Return Value  
 `true` if the `full` function of the max class returns `false`; otherwise, the `push` function returns `false`.  
  
## Remarks  
 If the `full` function of the max class returns `false`, this member function adds the memory block pointed to by `_Ptr` to the head of the list.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [freelist Class](../vs140/freelist-Class.md)