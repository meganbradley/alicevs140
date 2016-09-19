---
title: "CTypedPtrMap::RemoveKey"
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
ms.assetid: b40fe9f4-df19-4e20-87ff-62421e0dbf7c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrMap::RemoveKey
This member function calls `BASE_CLASS`**::RemoveKey**.  
  
## Syntax  
  
```  
  
      BOOL RemoveKey(  
   KEY key   
);  
```  
  
#### Parameters  
 *KEY*  
 Template parameter specifying the type of the map's keys.  
  
 `key`  
 Key for the element to be removed.  
  
## Return Value  
 Nonzero if the entry was found and successfully removed; otherwise 0.  
  
## Remarks  
 For more detailed remarks, see [CMapStringToOb::RemoveKey](../vs140/CMapStringToOb--RemoveKey.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrMap Class](../vs140/CTypedPtrMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)