---
title: "AfxDoForAllObjects"
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
ms.assetid: ef4ebe96-d254-4a9b-9dbb-6b8c760a6d80
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxDoForAllObjects
Executes the specified iteration function for all objects derived from `CObject` that have been allocated with **new**.  
  
## Syntax  
  
```  
  
      void AfxDoForAllObjects(  
   void (*pfn  
)(CObject* pObject,  
   void* pContext  
),  
   void* pContext   
);   
```  
  
#### Parameters  
 `pfn`  
 Points to an iteration function to execute for each object. The function arguments are a pointer to a `CObject` and a void pointer to extra data that the caller supplies to the function.  
  
 `pContext`  
 Points to optional data that the caller can supply to the iteration function. This pointer can be **NULL**.  
  
## Remarks  
 Stack, global, or embedded objects are not enumerated. The pointer passed to `AfxDoForAllObjects` in `pContext` is passed to the specified iteration function each time it is called.  
  
> [!NOTE]
>  This function works only in the Debug version of MFC.  
  
## Example  
 [!CODE [NVC_MFCCollections#115](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#115)]  
  
 [!CODE [NVC_MFCCollections#116](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#116)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)