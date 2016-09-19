---
title: "COleSafeArray::CreateOneDim"
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
ms.assetid: bf518930-d58a-4a7e-af40-335f147fd590
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::CreateOneDim
Creates a new one-dimensional `COleSafeArray` object.  
  
## Syntax  
  
```  
  
      void CreateOneDim(  
   VARTYPE vtSrc,  
   DWORD dwElements,  
   const void* pvSrcData = NULL,  
   long nLBound = 0   
);  
```  
  
#### Parameters  
 `vtSrc`  
 The base type of the array (that is, the **VARTYPE** of each element of the array).  
  
 `dwElements`  
 Number of elements in the array. This can be changed after the array is created with [ResizeOneDim](../vs140/COleSafeArray--ResizeOneDim.md).  
  
 `pvSrcData`  
 Pointer to the data to copy into the array.  
  
 *nLBound*  
 The lower bound of the array.  
  
## Remarks  
 The function allocates and initializes the data for the array, copying the specified data if the pointer `pvSrcData` is not **NULL**.  
  
 On error, the function throws a [CMemoryException](../vs140/CMemoryException-Class.md).  
  
## Example  
 [!CODE [NVC_MFCOleContainer#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#28)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::GetOneDimSize](../vs140/COleSafeArray--GetOneDimSize.md)   
 [COleSafeArray::ResizeOneDim](../vs140/COleSafeArray--ResizeOneDim.md)   
 [COleSafeArray::Create](../vs140/COleSafeArray--Create.md)