---
title: "CStockPropImpl::get_TabStop"
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
ms.assetid: 55eb4c14-1a49-4d45-8fb5-d12d3ada0c3c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_TabStop
Call this method to get the status of the flag that indicates if the control is a tab stop or not.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_TabStop(  
   VARIANT_BOOL * pbTabStop  
);  
```  
  
#### Parameters  
 *pbTabStop*  
 Variable that receives the flag status. TRUE indicates that the control is a tab stop.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_TabStop](../vs140/CStockPropImpl--put_TabStop.md)