---
title: "CArray::operator"
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
ms.assetid: c8704f88-22ed-4f93-ae8b-f80512e8d9eb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::operator
These subscript operators are a convenient substitute for the [SetAt](../vs140/CArray--SetAt.md) and [GetAt](../vs140/CArray--GetAt.md) functions.  
  
## Syntax  
  
```  
  
      TYPE  
      & operator[](INT_PTR nIndex);  
const TYPE& operator[](INT_PTR nIndex) const;  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements in this array.  
  
 `nIndex`  
 Index of the element to be accessed.  
  
## Remarks  
 The first operator, called for arrays that are not **const**, may be used on either the right (r-value) or the left (l-value) of an assignment statement. The second, called for **const** arrays, may be used only on the right.  
  
 The Debug version of the library asserts if the subscript (either on the left or right side of an assignment statement) is out of bounds.  
  
## Example  
 [!CODE [NVC_MFCCollections#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#34)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::GetAt](../vs140/CArray--GetAt.md)   
 [CArray::SetAt](../vs140/CArray--SetAt.md)   
 [CArray::ElementAt](../vs140/CArray--ElementAt.md)