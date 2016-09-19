---
title: "CComControlBase::GetAmbientSupportsMnemonics"
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
ms.assetid: 224bc1cc-ff93-46f9-b435-654e178f27fc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientSupportsMnemonics
Retrieves **DISPID_AMBIENT_SUPPORTSMNEMONICS**, a flag indicating whether the container supports keyboard mnemonics.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientSupportsMnemonics(  
   BOOL& bSupportsMnemonics  
);  
```  
  
#### Parameters  
 *bSupportsMnemonics*  
 The property **DISPID_AMBIENT_SUPPORTSMNEMONICS**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)