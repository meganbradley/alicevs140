---
title: "CRBTree::CPair Class"
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
ms.topic: reference
ms.assetid: 35e224ed-407e-4864-90ee-2dac2432ad41
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::CPair Class
A class containing the key and value elements.  
  
## Syntax  
  
```  
  
class CPair : public __POSITION  
  
```  
  
## Remarks  
 This class is used by the methods [CRBTree::GetAt](../vs140/CRBTree--GetAt.md), [CRBTree::GetNext](../vs140/CRBTree--GetNext.md), and [CRBTree::GetPrev](../vs140/CRBTree--GetPrev.md) to access the key and value elements stored in the tree structure.  
  
 The members are as follows:  
  
|||  
|-|-|  
|[m_key](../vs140/CAtlMap--CPair--m_key.md)|The data member storing the key element.|  
|[m_value](../vs140/CAtlMap--CPair--m_value.md)|The data member storing the value element.|  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)