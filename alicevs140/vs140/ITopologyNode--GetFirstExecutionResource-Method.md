---
title: "ITopologyNode::GetFirstExecutionResource Method"
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
ms.assetid: 3cb07fc8-71d4-4180-86e4-27f47af39efd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ITopologyNode::GetFirstExecutionResource Method
Returns the first execution resource grouped under this node in enumeration order.  
  
## Syntax  
  
```  
virtual ITopologyExecutionResource *GetFirstExecutionResource() const =0;  
```  
  
## Return Value  
 The first execution resource grouped under this node in enumeration order.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ITopologyNode Structure](../vs140/ITopologyNode-Structure.md)   
 [ITopologyNode::GetExecutionResourceCount Method](../vs140/ITopologyNode--GetExecutionResourceCount-Method.md)