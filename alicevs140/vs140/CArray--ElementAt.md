---
title: "CArray::ElementAt"
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
ms.assetid: 2daccef9-0bfe-473f-a302-a350db717c5a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::ElementAt
Returns a temporary reference to the specified element within the array.  
  
## Syntax  
  
```  
  
      TYPE& ElementAt(  
   INT_PTR nIndex   
);  
const TYPE& ElementAt(   
   INT_PTR nIndex  
) const;  
```  
  
#### Parameters  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by [GetUpperBound](../vs140/CArray--GetUpperBound.md).  
  
## Return Value  
 A reference to an array element.  
  
## Remarks  
 It is used to implement the left-side assignment operator for arrays.  
  
## Example  
 See the example for [GetSize](../vs140/CArray--GetSize.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::operator](../vs140/CArray--operator.md)