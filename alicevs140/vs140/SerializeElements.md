---
title: "SerializeElements"
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
ms.topic: article
ms.assetid: a5ccd494-40b5-4a1f-aba2-33748c00b7a0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SerializeElements
[CArray](../vs140/CArray-Class.md), [CList](../vs140/CList-Class.md), and [CMap](../vs140/CMap-Class.md) call this function to serialize elements.  
  
## Syntax  
  
```  
  
      template< class TYPE >   
void AFXAPI SerializeElements(  
   CArchive& ar,  
   TYPE* pElements,  
   INT_PTR nCount   
);  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of the elements.  
  
 `ar`  
 An archive object to archive to or from.  
  
 `pElements`  
 Pointer to the elements being archived.  
  
 `nCount`  
 Number of elements being archived  
  
## Remarks  
 The default implementation does a bitwise read or write.  
  
 For information on implementing this and other helper functions, see the article [Collections: How to Make a Type-Safe Collection](../vs140/How-to--Make-a-Type-Safe-Collection.md).  
  
## Example  
 See the example in the article [Collections: How to Make a Type-Safe Collection](../vs140/How-to--Make-a-Type-Safe-Collection.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CArchive Class](../vs140/CArchive-Class.md)