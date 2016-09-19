---
title: "CStockPropImpl::put_Text"
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
ms.assetid: 018b8d7b-0f3e-47f3-a24c-5fbad1145995
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_Text
Call this method to set the text that is displayed with the control.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_Text(  
   BSTR bstrText  
);  
```  
  
#### Parameters  
 `bstrText`  
 The text that is displayed with the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_Text](../vs140/CStockPropImpl--get_Text.md)