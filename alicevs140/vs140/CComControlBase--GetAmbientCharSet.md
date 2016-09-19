---
title: "CComControlBase::GetAmbientCharSet"
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
ms.assetid: 2be3c8a5-6387-4196-ae8d-e66a74c03867
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientCharSet
Retrieves **DISPID_AMBIENT_CHARSET**, the ambient character set for all controls, defined by the container.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientCharSet(  
   BSTR& bstrCharSet   
);  
```  
  
#### Parameters  
 *bstrCharSet*  
 The property **DISPID_AMBIENT_CHARSET**.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)