---
title: "CMapStringToOb::GetCount"
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
ms.assetid: 552a4f68-24d2-487c-b5ef-645f261019f6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::GetCount
Determines how many elements are in the map.  
  
## Syntax  
  
```  
  
INT_PTR GetCount( ) const;  
```  
  
## Return Value  
 The number of elements in this map.  
  
## Remarks  
 The following table shows other member functions that are similar to `CMapStringToOb::GetCount`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**INT_PTR GetCount( ) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#64](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#64)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToOb::IsEmpty](../vs140/CMapStringToOb--IsEmpty.md)