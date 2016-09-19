---
title: "ITopologyNode::GetNext Method"
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
ms.assetid: 463c2715-aa8c-4a0b-82af-e9ebeb5453da
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ITopologyNode::GetNext Method
Returns an interface to the next topology node in enumeration order.  
  
## Syntax  
  
```  
virtual ITopologyNode *GetNext() const =0;  
```  
  
## Return Value  
 An interface to the next node in enumeration order. If there are no more nodes in enumeration order of the system topology, this method will return the value `NULL`.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ITopologyNode Structure](../vs140/ITopologyNode-Structure.md)   
 [IResourceManager::GetFirstNode Method](../vs140/IResourceManager--GetFirstNode-Method.md)   
 [ITopologyExecutionResource Structure](../vs140/ITopologyExecutionResource-Structure.md)