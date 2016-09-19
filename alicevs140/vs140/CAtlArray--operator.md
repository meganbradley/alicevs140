---
title: "CAtlArray::operator"
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
ms.assetid: d2914763-300b-4af1-8a68-a3b47a5a494a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::operator
Call this operator to return a reference to an element in the array.  
  
## Syntax  
  
```  
  
      E& operator[](size_t iElement) throw( );  
const E& operator[](size_t iElement) const throw( );  
```  
  
#### Parameters  
 `iElement`  
 The index value of the array element to return.  
  
## Return Value  
 Returns a reference to the required array element.  
  
## Remarks  
 Performs a similar function to [CAtlArray::GetAt](../vs140/CAtlArray--GetAt.md). Unlike the MFC class [CArray](../vs140/CArray-Class.md), this operator cannot be used as a substitute for [CAtlArray::SetAt](../vs140/CAtlArray--SetAt.md).  
  
 In debug builds, an ATLASSERT will be raised if `iElement` exceeds the total number of elements in the array. In retail builds, an invalid parameter may cause unpredictable results.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)