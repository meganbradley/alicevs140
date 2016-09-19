---
title: "CTypedPtrMap::GetNextAssoc"
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
ms.assetid: 96652cce-12a4-4c18-98cd-093c1bb10c0e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrMap::GetNextAssoc
Retrieves the map element at `rNextPosition`, then updates `rNextPosition` to refer to the next element in the map.  
  
## Syntax  
  
```  
  
      void GetNextAssoc(  
   POSITION& rPosition,  
   KEY& rKey,  
   VALUE& rValue   
) const;  
```  
  
#### Parameters  
 `rPosition`  
 Specifies a reference to a **POSITION** value returned by a previous `GetNextAssoc` or `BASE_CLASS`**::GetStartPosition** call.  
  
 *KEY*  
 Template parameter specifying the type of the map's keys.  
  
 `rKey`  
 Specifies the returned key of the retrieved element.  
  
 *VALUE*  
 Template parameter specifying the type of the map's values.  
  
 `rValue`  
 Specifies the returned value of the retrieved element.  
  
## Remarks  
 This function is most useful for iterating through all the elements in the map. Note that the position sequence is not necessarily the same as the key value sequence.  
  
 If the retrieved element is the last in the map, then the new value of `rNextPosition` is set to **NULL**.  
  
 This inline function calls `BASE_CLASS`**::GetNextAssoc**.  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrMap Class](../vs140/CTypedPtrMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToOb::GetNextAssoc](../vs140/CMapStringToOb--GetNextAssoc.md)   
 [CMapStringToOb::GetStartPosition](../vs140/CMapStringToOb--GetStartPosition.md)