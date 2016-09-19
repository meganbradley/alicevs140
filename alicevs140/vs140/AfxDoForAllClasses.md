---
title: "AfxDoForAllClasses"
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
ms.assetid: 6e4f95bc-d679-4811-a2de-801b1bacf336
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxDoForAllClasses
Calls the specified iteration function for all serializable `CObject`-derived classes in the application's memory space.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxDoForAllClasses(  
   void (*pfn  
)(const CRuntimeClass* pClass,  
   void* pContext  
),  
   void* pContext   
);   
```  
  
#### Parameters  
 `pfn`  
 Points to an iteration function to be called for each class. The function arguments are a pointer to a `CRuntimeClass` object and a void pointer to extra data that the caller supplies to the function.  
  
 `pContext`  
 Points to optional data that the caller can supply to the iteration function. This pointer can be **NULL**.  
  
## Remarks  
 Serializable `CObject`-derived classes are classes derived using the `DECLARE_SERIAL` macro. The pointer that is passed to `AfxDoForAllClasses` in `pContext` is passed to the specified iteration function each time it is called.  
  
> [!NOTE]
>  This function works only in the Debug version of MFC.  
  
## Example  
 [!CODE [NVC_MFCCollections#113](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#113)]  
  
 [!CODE [NVC_MFCCollections#114](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#114)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md)