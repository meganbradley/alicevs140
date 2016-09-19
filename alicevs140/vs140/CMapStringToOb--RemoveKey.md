---
title: "CMapStringToOb::RemoveKey"
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
ms.assetid: 66ea5b21-6faf-429d-83a2-95d3cb9ed702
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::RemoveKey
Looks up the map entry corresponding to the supplied key; then, if the key is found, removes the entry.  
  
## Syntax  
  
```  
  
      BOOL RemoveKey(  
   LPCTSTR key   
);  
```  
  
#### Parameters  
 `key`  
 Specifies the string used for map lookup.  
  
## Return Value  
 Nonzero if the entry was found and successfully removed; otherwise 0.  
  
## Remarks  
 This can cause memory leaks if the `CObject` object is not deleted elsewhere.  
  
 The following table shows other member functions that are similar to `CMapStringToOb::RemoveKey`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**BOOL RemoveKey( void\***  `key`  **);**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**BOOL RemoveKey( void\***  `key`  **);**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**BOOL RemoveKey( LPCTSTR**  `key`  **);**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**BOOL RemoveKey( LPCTSTR**  `key`  **);**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**BOOL RemoveKey( WORD**  `key`  **);**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**BOOL RemoveKey( WORD**  `key`  **);**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#70](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#70)]  
  
 The results from this program are as follows:  
  
 `RemoveKey example: A CMapStringToOb with 3 elements`  
  
 `[Marge] = a CAge at $49A0 35`  
  
 `[Homer] = a CAge at $495E 36`  
  
 `[Bart] = a CAge at $4634 13`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToOb::RemoveAll](../vs140/CMapStringToOb--RemoveAll.md)