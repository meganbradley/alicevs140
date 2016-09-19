---
title: "CAxDialogImpl::AdviseSinkMap"
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
ms.assetid: 661a575c-cf65-493a-8970-58e439b7b149
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxDialogImpl::AdviseSinkMap
Call this method to advise or unadvise all entries in the object's sink map event map.  
  
## Syntax  
  
```  
  
      HRESULT AdviseSinkMap(  
   bool bAdvise   
);  
```  
  
#### Parameters  
 `bAdvise`  
 Set to true if all sink entries are to be advised; false if all sink entries are to be unadvised.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxDialogImpl Class](../vs140/CAxDialogImpl-Class.md)