---
title: "CAtlArray::InsertArrayAt"
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
ms.assetid: 95e01539-80d9-4451-910a-96282ab1806c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::InsertArrayAt
Call this method to insert one array into another.  
  
## Syntax  
  
```  
  
      void InsertArrayAt(  
   size_t iStart,  
   const CAtlArray< E, ETraits >* paNew   
);  
```  
  
#### Parameters  
 `iStart`  
 The index at which the array is to be inserted.  
  
 `paNew`  
 The array to be inserted.  
  
## Remarks  
 Elements from the array `paNew` are copied into the array object, beginning at element `iStart`. The existing array elements are moved to avoid being overwritten.  
  
 In debug builds, an ATLASSERT will be raised if the `CAtlArray` object is not valid, or if the `paNew` pointer is NULL or invalid.  
  
> [!NOTE]
>  `CAtlArray::InsertArrayAt` does not support arrays consisting of elements created with the [CAutoPtr](../vs140/CAutoPtr-Class.md) class.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#8](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#8)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::Append](../vs140/CAtlArray--Append.md)