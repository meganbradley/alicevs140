---
title: "CMapStringToOb::GetSize"
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
ms.assetid: 5d9ae412-3998-4da1-b947-ee7298149ad5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::GetSize
Returns the number of map elements.  
  
## Syntax  
  
```  
  
INT_PTR GetSize( ) const;  
```  
  
## Return Value  
 The number of items in the map.  
  
## Remarks  
 Call this method to retrieve the number of elements in the map.  
  
 The following table shows other member functions that are similar to `CMapStringToOb::GetSize`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**INT_PTR GetSize( ) const;**|  
  
## Example  
 [!CODE [NVC_MFCCollections#67](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#67)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)