---
title: "CStockPropImpl::put_Caption"
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
ms.assetid: 381ce56c-d55d-4e0c-89b1-8e8fbd781eaf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_Caption
Call this method to set the text to be displayed with the control.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_Caption(  
   BSTR bstrCaption  
);  
```  
  
#### Parameters  
 *bstrCaption*  
 The text to be displayed with the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_Caption](../vs140/CStockPropImpl--get_Caption.md)