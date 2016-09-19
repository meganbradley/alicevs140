---
title: "CMap::operator"
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
ms.assetid: 4f300572-3eff-4ca9-b052-444f7d6699a1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::operator
A convenient substitute for the `SetAt` member function.  
  
## Syntax  
  
```  
  
      VALUE  
      & operator[](ARG_KEY key);  
```  
  
#### Parameters  
 *VALUE*  
 Template parameter specifying the type of the map value.  
  
 `ARG_KEY`  
 Template parameter specifying the type of the key value.  
  
 `key`  
 The key used to retrieve the value from the map.  
  
## Remarks  
 Thus it can be used only on the left side of an assignment statement (an l-value). If there is no map element with the specified key, then a new element is created.  
  
 There is no "right side" (r-value) equivalent to this operator because there is a possibility that a key may not be found in the map. Use the `Lookup` member function for element retrieval.  
  
## Example  
 See the example for [CMap::Lookup](../vs140/CMap--Lookup.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMap::SetAt](../vs140/CMap--SetAt.md)   
 [CMap::Lookup](../vs140/CMap--Lookup.md)