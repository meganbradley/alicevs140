---
title: "CStockPropImpl::get_Text"
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
ms.assetid: dc571481-bcf1-4f99-943b-7f95294e7b00
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_Text
Call this method to get the text that is displayed with the control.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_Text(  
   BSTR * pbstrText  
);  
```  
  
#### Parameters  
 *pbstrText*  
 The text that is displayed with the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_Text](../vs140/CStockPropImpl--put_Text.md)