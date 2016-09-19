---
title: "CStockPropImpl::get_AutoSize"
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
ms.assetid: e55eb416-6c03-4a54-b0f2-e1db202c016c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_AutoSize
Call this method to get the status of the flag that indicates if the control cannot be any other size.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_Autosize(  
   VARIANT_BOOL * pbAutoSize  
);  
```  
  
#### Parameters  
 *pbAutoSize*  
 Variable that receives the flag status. TRUE indicates that the control cannot be any other size.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_AutoSize](../vs140/CStockPropImpl--put_AutoSize.md)