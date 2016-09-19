---
title: "CMapStringToOb::LookupKey"
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
ms.assetid: 023d7f48-a0a4-445c-b12e-19cb7fc9e5d1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::LookupKey
Returns a reference to the key associated with the specified key value.  
  
## Syntax  
  
```  
  
      BOOL LookupKey(  
   LPCTSTR key,  
   LPCTSTR& rKey  
) const;  
```  
  
#### Parameters  
 `key`  
 Specifies the string key that identifies the element to be looked up.  
  
 `rKey`  
 The reference to the associated key.  
  
## Return Value  
 Nonzero if the key was found; otherwise 0.  
  
## Remarks  
 Using a reference to a key is unsafe if used after the associated element was removed from the map or after the map was destroyed.  
  
 The following table shows other member functions that are similar to **CMapStringToOb:: LookupKey**.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**BOOL LookupKey( LPCTSTR**  `key` **, LPCTSTR&** `rKey`  **) const;**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**BOOL LookupKey( LPCTSTR**  `key` **, LPCTSTR&** `rKey`  **) const;**|  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)