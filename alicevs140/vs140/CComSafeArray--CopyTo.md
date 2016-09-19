---
title: "CComSafeArray::CopyTo"
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
ms.assetid: e256e290-c00c-4f80-ba5a-8d1d5ce50a39
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArray::CopyTo
Creates a copy of the `CComSafeArray` object.  
  
## Syntax  
  
```  
  
      HRESULT CopyTo(  
   LPSAFEARRAY * ppArray   
);  
```  
  
#### Parameters  
 `ppArray`  
 A pointer to a location in which to create the new **SAFEARRAY**.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method copies the contents of a `CComSafeArray` object into a **SAFEARRAY** structure.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArray Class](../vs140/CComSafeArray-Class.md)   
 [CComSafeArray::CopyFrom](../vs140/CComSafeArray--CopyFrom.md)