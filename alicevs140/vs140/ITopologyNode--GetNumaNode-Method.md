---
title: "ITopologyNode::GetNumaNode Method"
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
ms.assetid: efe83674-c399-496d-90c0-da52558ba031
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ITopologyNode::GetNumaNode Method
Returns the Windows assigned NUMA node number to which this Resource Maanger node belongs.  
  
## Syntax  
  
```  
virtual unsigned long GetNumaNode() const =0;  
```  
  
## Return Value  
 The Windows assigned NUMA node number to which this Resource Manager node belongs.  
  
## Remarks  
 A thread proxy running on a virtual processor root belonging to this node will have affinity to at least the NUMA node level for the NUMA node returned by this method.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ITopologyNode Structure](../vs140/ITopologyNode-Structure.md)