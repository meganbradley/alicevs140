---
title: "CComControlBase::PreTranslateAccelerator"
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
ms.assetid: dd435ab4-ee7f-4453-85ad-5f391c2bf67e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::PreTranslateAccelerator
Override this method to provide your own keyboard accelerator handlers.  
  
## Syntax  
  
```  
  
      BOOL PreTranslateAccelerator(  
   LPMSG /* pMsg */,  
   HRESULT& /* hRet */  
);  
```  
  
#### Parameters  
 `pMsg`  
 Reserved.  
  
 *hRet*  
 Reserved.  
  
## Return Value  
 By default returns **FALSE**.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)