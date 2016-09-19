---
title: "CMapStringToOb::Lookup"
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
ms.assetid: 3982769d-4d5f-413e-b27b-2075fd3593b1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::Lookup
Returns a `CObject` pointer based on a `CString` value.  
  
## Syntax  
  
```  
  
      BOOL Lookup(  
   LPCTSTR key,  
   CObject*& rValue   
) const;  
```  
  
#### Parameters  
 `key`  
 Specifies the string key that identifies the element to be looked up.  
  
 `rValue`  
 Specifies the returned value from the looked-up element.  
  
## Return Value  
 Nonzero if the element was found; otherwise 0.  
  
## Remarks  
 `Lookup` uses a hashing algorithm to quickly find the map element with a key that matches exactly (`CString` value).  
  
 The following table shows other member functions that are similar to `CMapStringToOb::LookUp`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**BOOL Lookup( void\***  `key` **, void\*&**  `rValue`  **) const;**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**BOOL Lookup( void\***  `key` **, WORD&**  `rValue`  **) const;**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**BOOL Lookup( LPCTSTR**  `key` **, void\*&**  `rValue`  **) const;**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**BOOL Lookup( LPCTSTR**  `key` **, CString&**  `rValue`  **) const;**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**BOOL Lookup( WORD**  `key` **, CObject\*&**  `rValue`  **) const;**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**BOOL Lookup( WORD**  `key` **, void\*&**  `rValue`  **) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#68](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#68)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToOb::operator](../vs140/CMapStringToOb--operator.md)