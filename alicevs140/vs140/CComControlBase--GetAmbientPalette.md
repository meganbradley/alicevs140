---
title: "CComControlBase::GetAmbientPalette"
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
ms.assetid: 0bb8e45f-ca48-4349-b9c1-37d9ad67c172
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientPalette
Retrieves **DISPID_AMBIENT_PALETTE**, used to access the container's `HPALETTE`.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientPalette(  
   HPALETTE& hPalette  
);  
```  
  
#### Parameters  
 `hPalette`  
 The property **DISPID_AMBIENT_PALETTE**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)