---
title: "CAxWindow::SetExternalDispatch"
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
ms.assetid: 63ee703f-afe5-49a3-9f1e-f5f90057ed31
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxWindow::SetExternalDispatch
Sets the external dispatch interface for the `CAxWindow` object.  
  
## Syntax  
  
```  
  
      HRESULT SetExternalDispatch(  
   IDispatch* pDisp   
);  
```  
  
#### Parameters  
 `pDisp`  
 [in] A pointer to an `IDispatch` interface.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxWindow Class](../vs140/CAxWindow-Class.md)   
 [CAxWindow::SetExternalUIHandler](../vs140/CAxWindow--SetExternalUIHandler.md)