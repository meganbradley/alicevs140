---
title: "CMap::CPair"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 55f47198-498d-4c67-8829-4c40e1250593
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::CPair
Contains a key value and the value of the associated object.  
  
## Remarks  
 This is a nested structure within class [CMap](../vs140/CMap-Class.md).  
  
 The structure is composed of two fields:  
  
-   **key** The actual value of the key type.  
  
-   **value** The value of the associated object.  
  
 It is used to store the return values from [CMap::PLookup](../vs140/CMap--PLookup.md), [CMap::PGetFirstAssoc](../vs140/CMap--PGetFirstAssoc.md), and [CMap::PGetNextAssoc](../vs140/CMap--PGetNextAssoc.md).  
  
## Example  
 For an example of usage, see the example for [CMap::PLookup](../vs140/CMap--PLookup.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)