---
title: "CComControlBase::GetAmbientAppearance"
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
ms.assetid: 88e8087b-141f-4998-9eba-8e6d07265c29
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientAppearance
Retrieves **DISPID_AMBIENT_APPEARANCE**, the current appearance setting for the control: 0 for flat and 1 for 3D.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientAppearance(  
   short& nAppearance  
);   
```  
  
#### Parameters  
 `nAppearance`  
 The property **DISPID_AMBIENT_APPEARANCE**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Example  
 [!CODE [NVC_ATL_COM#22](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#22)]  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)