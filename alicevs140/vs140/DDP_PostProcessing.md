---
title: "DDP_PostProcessing"
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
ms.assetid: abafd331-8eec-40d7-b39c-9bcbab2757be
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDP_PostProcessing
Call this function in your property page's `DoDataExchange` function, to finish the transfer of property values from the property page to your control when property values are being saved.  
  
## Syntax  
  
```  
  
      void AFXAPI DDP_PostProcessing(  
   CDataExchange *pDX   
);  
```  
  
#### Parameters  
 `pDX`  
 Pointer to a `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
## Remarks  
 This function should be called after all data exchange functions are completed. For example:  
  
 [!CODE [NVC_MFCAxCtl#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#15)]  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)