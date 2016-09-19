---
title: "CMapStringToOb::SetAt"
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
ms.assetid: 4ab4288b-f95a-4d86-b7c9-48f82845e726
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::SetAt
The primary means to insert an element in a map.  
  
## Syntax  
  
```  
  
      void SetAt(  
   LPCTSTR key,  
   CObject* newValue   
);  
```  
  
#### Parameters  
 `key`  
 Specifies the string that is the key of the new element.  
  
 `newValue`  
 Specifies the `CObject` pointer that is the value of the new element.  
  
## Remarks  
 First, the key is looked up. If the key is found, then the corresponding value is changed; otherwise a new key-value element is created.  
  
 The following table shows other member functions that are similar to `CMapStringToOb::SetAt`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**void SetAt( void\***  `key` **, void\***  `newValue`  **);**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**void SetAt( void\***  `key` **, WORD**  `newValue`  **);**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**void SetAt( LPCTSTR**  `key` **, void\***  `newValue`  **);**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**void SetAt( LPCTSTR**  `key` **, LPCTSTR**  `newValue`  **);**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**void SetAt( WORD**  `key` **, CObject\***  `newValue`  **);**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**void SetAt( WORD**  `key` **, void\***  `newValue`  **);**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#71](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#71)]  
  
 The results from this program are as follows:  
  
 `before Lisa's birthday: A CMapStringToOb with 2 elements`  
  
 `[Lisa] = a CAge at $493C 11`  
  
 `[Bart] = a CAge at $4654 13`  
  
 `after Lisa's birthday: A CMapStringToOb with 2 elements`  
  
 `[Lisa] = a CAge at $49C0 12`  
  
 `[Bart] = a CAge at $4654 13`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToOb::Lookup](../vs140/CMapStringToOb--Lookup.md)   
 [CMapStringToOb::operator](../vs140/CMapStringToOb--operator.md)