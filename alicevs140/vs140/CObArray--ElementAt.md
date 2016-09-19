---
title: "CObArray::ElementAt"
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
ms.assetid: 4d3b0e92-dd84-4015-8e8e-b9dec3fda412
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::ElementAt
Returns a temporary reference to the element pointer within the array.  
  
## Syntax  
  
```  
  
      CObject*& ElementAt(  
   INT_PTR nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by `GetUpperBound`.  
  
## Return Value  
 A reference to a `CObject` pointer.  
  
## Remarks  
 It is used to implement the left-side assignment operator for arrays. Note that this is an advanced function that should be used only to implement special array operators.  
  
 The following table shows other member functions that are similar to `CObArray::ElementAt`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**BYTE& ElementAt( INT_PTR** `nIndex` **);**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**DWORD& ElementAt( INT_PTR** `nIndex` **);**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**void\*& ElementAt( INT_PTR** `nIndex` **);**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**CString& ElementAt( INT_PTR** `nIndex` **);**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**UINT& ElementAt( INT_PTR** `nIndex` **);**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**WORD& ElementAt( INT_PTR** `nIndex` **);**|  
  
## Example  
 See the example for [CObArray::GetSize](../vs140/CObArray--GetSize.md).  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::operator](../vs140/CObArray--operator.md)