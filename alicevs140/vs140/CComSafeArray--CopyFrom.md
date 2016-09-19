---
title: "CComSafeArray::CopyFrom"
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
ms.assetid: 3546cfaa-3fa0-4494-a4c9-6acbb2ac5c5f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArray::CopyFrom
Copies the contents of a **SAFEARRAY** structure into the `CComSafeArray` object.  
  
## Syntax  
  
```  
  
      HRESULT CopyFrom(  
   LPSAFEARRAY * ppArray   
);  
```  
  
#### Parameters  
 `ppArray`  
 Pointer to the **SAFEARRAY** to copy.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method copies the contents of a **SAFEARRAY** into the current `CComSafeArray` object. The existing contents of the array are replaced.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArray Class](../vs140/CComSafeArray-Class.md)   
 [CComSafeArray::CopyTo](../vs140/CComSafeArray--CopyTo.md)