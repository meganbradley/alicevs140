---
title: "CMap::GetNextAssoc"
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
ms.assetid: c5574410-587f-4c31-8c37-6b51a5616c56
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::GetNextAssoc
Retrieves the map element at `rNextPosition`, then updates `rNextPosition` to refer to the next element in the map.  
  
## Syntax  
  
```  
  
      void GetNextAssoc(  
   POSITION& rNextPosition,  
   KEY& rKey,  
   VALUE& rValue   
) const;  
```  
  
#### Parameters  
 `rNextPosition`  
 Specifies a reference to a **POSITION** value returned by a previous `GetNextAssoc` or `GetStartPosition` call.  
  
 *KEY*  
 Template parameter specifying the type of the map's key.  
  
 `rKey`  
 Specifies the returned key of the retrieved element.  
  
 *VALUE*  
 Template parameter specifying the type of the map's value.  
  
 `rValue`  
 Specifies the returned value of the retrieved element.  
  
## Remarks  
 This function is most useful for iterating through all the elements in the map. Note that the position sequence is not necessarily the same as the key value sequence.  
  
 If the retrieved element is the last in the map, then the new value of `rNextPosition` is set to **NULL**.  
  
## Example  
 See the example for [CMap::SetAt](../vs140/CMap--SetAt.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMap::GetStartPosition](../vs140/CMap--GetStartPosition.md)