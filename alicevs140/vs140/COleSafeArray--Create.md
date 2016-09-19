---
title: "COleSafeArray::Create"
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
ms.assetid: b3341152-2774-44ff-b709-3132f26f1311
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::Create
Allocates and initializes the data for the array.  
  
## Syntax  
  
```  
  
      void Create(  
   VARTYPE vtSrc,  
   DWORD dwDims,  
   DWORD* rgElements   
);  
void Create(  
   VARTYPE vtSrc,  
   DWORD dwDims,  
   SAFEARRAYBOUND* rgsabounds   
);  
```  
  
#### Parameters  
 `vtSrc`  
 The base type of the array (that is, the **VARTYPE** of each element of the array). The **VARTYPE** is restricted to a subset of the variant types. Neither the **VT_ARRAY** nor the **VT_BYREF** flag can be set. `VT_EMPTY` and **VT_NULL** are not valid base types for the array. All other types are legal.  
  
 `dwDims`  
 Number of dimensions in the array. This can be changed after the array is created with [Redim](../vs140/COleSafeArray--Redim.md).  
  
 *rgElements*  
 Pointer to an array of the number of elements for each dimension in the array.  
  
 *rgsabounds*  
 Pointer to a vector of bounds (one for each dimension) to allocate for the array.  
  
## Remarks  
 This function will clear the current array data if necessary. On error, the function throws a [CMemoryException](../vs140/CMemoryException-Class.md).  
  
## Example  
 [!CODE [NVC_MFCOleContainer#27](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#27)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [SafeArrayCreate](assetId:///5b94f1a2-a558-473f-85dd-9545c0464cc7)