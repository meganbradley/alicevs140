---
title: "CComControlBase::GetAmbientScaleUnits"
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
ms.assetid: 9c155622-1924-4306-9f5c-558b42dd28e3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientScaleUnits
Retrieves **DISPID_AMBIENT_SCALEUNITS**, the container's ambient units (such as inches or centimeters) for labeling displays.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientScaleUnits(  
   BSTR& bstrScaleUnits  
);   
```  
  
#### Parameters  
 *bstrScaleUnits*  
 The property **DISPID_AMBIENT_SCALEUNITS**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)