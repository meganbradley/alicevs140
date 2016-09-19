---
title: "CArray::GetUpperBound"
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
ms.assetid: fa9a5309-4df7-44c4-9cfd-edc2495d45dc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::GetUpperBound
Returns the current upper bound of this array.  
  
## Syntax  
  
```  
  
INT_PTR GetUpperBound( ) const;  
```  
  
## Remarks  
 Because array indexes are zero-based, this function returns a value 1 less than `GetSize`.  
  
 The condition **GetUpperBound( )** = –1 indicates that the array contains no elements.  
  
## Example  
 See the example for [CArray::GetAt](../vs140/CArray--GetAt.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::GetSize](../vs140/CArray--GetSize.md)   
 [CArray::SetSize](../vs140/CArray--SetSize.md)