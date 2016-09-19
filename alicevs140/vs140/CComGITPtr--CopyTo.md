---
title: "CComGITPtr::CopyTo"
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
ms.assetid: 5580c156-0e69-400b-85e3-2fc77c9df16f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComGITPtr::CopyTo
Call this method to copy the interface from the global interface table (GIT) to the passed pointer.  
  
## Syntax  
  
```  
  
      HRESULT CopyTo(  
   T** pp   
) const throw( );  
```  
  
#### Parameters  
 `pp`  
 The pointer which is to receive the interface.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 The interface from the GIT is copied to the passed pointer. The pointer must be released by the caller when it is no longer required.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComGITPtr Class](../vs140/CComGITPtr-Class.md)