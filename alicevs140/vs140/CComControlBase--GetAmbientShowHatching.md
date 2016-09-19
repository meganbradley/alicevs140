---
title: "CComControlBase::GetAmbientShowHatching"
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
ms.assetid: 106f3470-c9c0-4fd7-b606-b6c404efe17f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientShowHatching
Retrieves **DISPID_AMBIENT_SHOWHATCHING**, a flag indicating whether the container allows the control to display itself with a hatched pattern when the control's user interface is active.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientShowHatching(  
   BOOL& bShowHatching  
);  
```  
  
#### Parameters  
 *bShowHatching*  
 The property **DISPID_AMBIENT_SHOWHATCHING**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)