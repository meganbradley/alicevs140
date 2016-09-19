---
title: "CStockPropImpl::get_Caption"
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
ms.assetid: 884c3290-0b15-421d-b0cf-a380fb216213
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_Caption
Call this method to get the text specified in an object's caption.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_Caption(  
   BSTR * pbstrCaption  
);  
```  
  
#### Parameters  
 *pbstrCaption*  
 The text to be displayed with the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_Caption](../vs140/CStockPropImpl--put_Caption.md)