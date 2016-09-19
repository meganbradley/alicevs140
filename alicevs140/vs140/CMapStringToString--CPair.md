---
title: "CMapStringToString::CPair"
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
ms.assetid: ebe8739b-10af-48ae-a36f-188f6315bfd6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToString::CPair
Contains a key value and the value of the associated string object.  
  
## Remarks  
 This is a nested structure within class [CMapStringToString](../vs140/CMapStringToString-Class.md).  
  
 The structure is composed of two fields:  
  
-   **key** The actual value of the key type.  
  
-   **value** The value of the associated object.  
  
 It is used to store the return values from [CMapStringToString::PLookup](../vs140/CMapStringToString--PLookup.md), [CMapStringToString::PGetFirstAssoc](../vs140/CMapStringToString--PGetFirstAssoc.md), and [CMapStringToString::PGetNextAssoc](../vs140/CMapStringToString--PGetNextAssoc.md).  
  
## Example  
 For an example of usage, see the example for [CMapStringToString::PLookup](../vs140/CMapStringToString--PLookup.md).  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToString Class](../vs140/CMapStringToString-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)