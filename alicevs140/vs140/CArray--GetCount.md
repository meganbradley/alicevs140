---
title: "CArray::GetCount"
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
ms.assetid: 15824ec1-8d10-4fc6-8221-bdfa43e54bdb
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::GetCount
Returns the number of array elements.  
  
## Syntax  
  
```  
  
INT_PTR GetCount( ) const;  
```  
  
## Return Value  
 The number of items in the array.  
  
## Remarks  
 Call this method to retrieve the number of elements in the array. Because indexes are zero-based, the size is 1 greater than the largest index. Calling this method will generate the same result as the [CArray::GetSize](../vs140/CArray--GetSize.md) method.  
  
## Example  
 [!CODE [NVC_MFCCollections#27](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#27)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::GetUpperBound](../vs140/CArray--GetUpperBound.md)   
 [CArray::SetSize](../vs140/CArray--SetSize.md)   
 [CArray::GetSize](../vs140/CArray--GetSize.md)