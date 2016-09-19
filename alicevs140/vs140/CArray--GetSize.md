---
title: "CArray::GetSize"
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
ms.assetid: a8b8c484-a66c-48bf-9cc3-c177a2525734
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::GetSize
Returns the size of the array.  
  
## Syntax  
  
```  
  
INT_PTR GetSize( ) const;  
```  
  
## Remarks  
 Because indexes are zero-based, the size is 1 greater than the largest index. Calling this method will generate the same result as the [CArray::GetCount](../vs140/CArray--GetCount.md) method.  
  
## Example  
 [!CODE [NVC_MFCCollections#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#29)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::GetUpperBound](../vs140/CArray--GetUpperBound.md)   
 [CArray::GetCount](../vs140/CArray--GetCount.md)