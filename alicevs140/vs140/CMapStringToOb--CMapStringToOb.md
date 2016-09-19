---
title: "CMapStringToOb::CMapStringToOb"
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
ms.assetid: 6528521d-a2e8-4c22-906e-2fba2a8604b9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::CMapStringToOb
Constructs an empty `CString`-to-`CObject*` map.  
  
## Syntax  
  
```  
  
      CMapStringToOb(  
   INT_PTR nBlockSize = 10   
);  
```  
  
#### Parameters  
 `nBlockSize`  
 Specifies the memory-allocation granularity for extending the map.  
  
## Remarks  
 As the map grows, memory is allocated in units of `nBlockSize` entries.  
  
 The following table shows other member functions that are similar to **CMapStringToOb:: CMapStringToOb**.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**CMapPtrToPtr( INT_PTR**  `nBlockSize`  **= 10 );**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**CMapPtrToWord( INT_PTR**  `nBlockSize`  **= 10 );**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**CMapStringToPtr( INT_PTR**  `nBlockSize`  **= 10 );**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**CMapStringToString( INT_PTR**  `nBlockSize`  **= 10 );**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**CMapWordToOb( INT_PTR**  `nBlockSize`  **= 10 );**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**MapWordToPtr( INT_PTR**  `nBlockSize`  **= 10 );**|  
  
## Example  
 [!CODE [NVC_MFCCollections#63](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#63)]  
  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)