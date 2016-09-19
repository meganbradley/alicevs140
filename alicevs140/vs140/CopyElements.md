---
title: "CopyElements"
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
ms.assetid: 2232a477-19c7-4512-8fd5-d31b8cd87c82
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CopyElements
This function is called directly by [CArray::Append](../vs140/CArray--Append.md) and [CArray::Copy](../vs140/CArray--Copy.md).  
  
## Syntax  
  
```  
  
      template<class   
      TYPE  
      >  
void AFXAPI CopyElements(  
   TYPE* pDest,  
   const TYPE* pSrc,  
   INT_PTR nCount   
);  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements to be copied.  
  
 `pDest`  
 Pointer to the destination where the elements will be copied.  
  
 `pSrc`  
 Pointer to the source of the elements to be copied.  
  
 `nCount`  
 Number of elements to be copied.  
  
## Remarks  
 The default implementation uses the simple assignment operator ( **=** ) to perform the copy operation. If the type being copied does not have an overloaded operator=, then the default implementation performs a bitwise copy.  
  
 For information on implementing this and other helper functions, see the article [Collections: How to Make a Type-Safe Collection](../vs140/How-to--Make-a-Type-Safe-Collection.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CArray Class](../vs140/CArray-Class.md)