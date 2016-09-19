---
title: "CMapStringToOb::HashKey"
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
ms.assetid: 3c2673ab-3abd-4d12-a72d-20c2cbc7d4d0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::HashKey
Calculates the hash value of a specified key.  
  
## Syntax  
  
```  
  
      UINT HashKey(  
   LPCTSTR key  
) const;  
```  
  
#### Parameters  
 `key`  
 The key whose hash value is to be calculated.  
  
## Return Value  
 The Key's hash value  
  
## Remarks  
 The following table shows other member functions that are similar to `CMapStringToOb::HashKey`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**UINT HashKey( void\***  `key`  **) const;**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**UINT HashKey( void\***  `key`  **) const;**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**UINT HashKey( LPCTSTR**  `key`  **) const;**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**UINT HashKey( LPCTSTR**  `key`  **) const;**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**UINT HashKey( WORD**  `key`  **) const;**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**UINT HashKey( WORD**  `key`  **) const;**|  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)