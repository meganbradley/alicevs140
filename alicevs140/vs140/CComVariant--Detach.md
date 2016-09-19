---
title: "CComVariant::Detach"
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
ms.assetid: 3c847834-3dbb-41b7-8066-2d7fcae6c65f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComVariant::Detach
Detaches the underlying **VARIANT** from the `CComVariant` object and sets the object's type to `VT_EMPTY`.  
  
## Syntax  
  
```  
  
      HRESULT Detach(  
   VARIANT* pDest   
);  
```  
  
#### Parameters  
 `pDest`  
 [out] Returns the underlying `VARIANT` value of the object.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 Note that the contents of the `VARIANT` referenced by `pDest` will automatically be cleared before being assigned the value and type of the calling **CComVariant** object.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComVariant Class](../vs140/CComVariant-Class.md)   
 [CComVariant::Attach](../vs140/CComVariant--Attach.md)