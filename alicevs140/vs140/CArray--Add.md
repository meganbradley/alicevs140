---
title: "CArray::Add"
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
ms.assetid: 0f790120-ffb2-4e56-b652-eb82517b48be
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::Add
Adds a new element to the end of an array, growing the array by 1.  
  
## Syntax  
  
```  
  
      INT_PTR Add(  
   ARG_TYPE newElement   
);  
```  
  
#### Parameters  
 `ARG_TYPE`  
 Template parameter specifying the type of arguments referencing elements in this array.  
  
 `newElement`  
 The element to be added to this array.  
  
## Return Value  
 The index of the added element.  
  
## Remarks  
 If [SetSize](../vs140/CArray--SetSize.md) has been used with an `nGrowBy` value greater than 1, then extra memory may be allocated. However, the upper bound will increase by only 1.  
  
## Example  
 [!CODE [NVC_MFCCollections#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#22)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::SetAt](../vs140/CArray--SetAt.md)   
 [CArray::SetAtGrow](../vs140/CArray--SetAtGrow.md)   
 [CArray::InsertAt](../vs140/CArray--InsertAt.md)   
 [CArray::operator](../vs140/CArray--operator.md)