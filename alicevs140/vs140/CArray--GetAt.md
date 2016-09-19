---
title: "CArray::GetAt"
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
ms.assetid: 09ba11c4-8167-41a4-9d78-cfa0116063f5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::GetAt
Returns the array element at the specified index.  
  
## Syntax  
  
```  
  
      TYPE  
      & GetAt(   
   INT_PTR nIndex    
);  
const TYPE& GetAt(   
   INT_PTR nIndex  
) const;  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of the array elements.  
  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by [GetUpperBound](../vs140/CArray--GetUpperBound.md).  
  
## Return Value  
 The array element currently at this index.  
  
## Remarks  
 Passing a negative value or a value greater than the value returned by `GetUpperBound` will result in a failed assertion.  
  
## Example  
 [!CODE [NVC_MFCCollections#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#26)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::SetAt](../vs140/CArray--SetAt.md)   
 [CArray::operator](../vs140/CArray--operator.md)