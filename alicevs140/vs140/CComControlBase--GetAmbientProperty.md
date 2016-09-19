---
title: "CComControlBase::GetAmbientProperty"
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
ms.assetid: 3bb0b59a-37f9-4117-94cc-dfd99d8db731
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientProperty
Retrieves the container property specified by `dispid`.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientProperty(  
   DISPID dispid,  
   VARIANT& var   
);  
```  
  
#### Parameters  
 `dispid`  
 Identifier of the container property to be retrieved.  
  
 `var`  
 Variable to receive the property.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Remarks  
 ATL has provided a set of helper functions to retrieve specific properties, for example, [CComControlBase::GetAmbientBackColor](../vs140/CComControlBase--GetAmbientBackColor.md). If there is no suitable method available, use `GetAmbientProperty`.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)