---
title: "CAtlArray::SetAt"
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
ms.assetid: d9ff1cfa-cdc2-4d91-9aa7-60fa102496f6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::SetAt
Call this method to set the value of an element in the array object.  
  
## Syntax  
  
```  
  
      void SetAt(  
   size_t iElement,  
   INARGTYPE element   
);  
```  
  
#### Parameters  
 `iElement`  
 The index pointing to the array element to set.  
  
 `element`  
 The new value of the specified element.  
  
## Remarks  
 In debug builds, an ATLASSERT will be raised if `iElement` exceeds the number of elements in the array. In retail builds, an invalid parameter may result in unpredictable results.  
  
## Example  
 See the example for [CAtlArray::GetAt](../vs140/CAtlArray--GetAt.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::GetAt](../vs140/CAtlArray--GetAt.md)   
 [CAtlArray::SetAtGrow](../vs140/CAtlArray--SetAtGrow.md)