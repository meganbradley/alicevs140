---
title: "CStockPropImpl::put_AutoSize"
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
ms.assetid: e708e3d1-c117-4f5c-8e36-cdcbfe3605b8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_AutoSize
Call this method to set the value of flag that indicates if the control cannot be any other size.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_AutoSize(  
   VARIANT_BOOL bAutoSize,  
);  
```  
  
#### Parameters  
 *bAutoSize*  
 TRUE if the control cannot be any other size.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_AutoSize](../vs140/CStockPropImpl--get_AutoSize.md)