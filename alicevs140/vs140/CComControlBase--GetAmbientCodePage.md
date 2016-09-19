---
title: "CComControlBase::GetAmbientCodePage"
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
ms.assetid: f8afec37-84bf-4451-a54d-fd15bc52ab8a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientCodePage
Retrieves **DISPID_AMBIENT_CODEPAGE**, the ambient code page for all controls, defined by the container.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientCodePage(  
   ULONG& ulCodePage   
);  
```  
  
#### Parameters  
 *ulCodePage*  
 The property **DISPID_AMBIENT_CODEPAGE**.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)