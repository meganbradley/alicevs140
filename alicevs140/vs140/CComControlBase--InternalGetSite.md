---
title: "CComControlBase::InternalGetSite"
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
ms.assetid: ed0d9be1-33aa-4270-a0a2-0b52e4da5041
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::InternalGetSite
Call this method to query the control site for a pointer to the identified interface.  
  
## Syntax  
  
```  
  
      HRESULT InternalGetSite(  
   REFIID riid,  
   void** ppUnkSite   
);  
```  
  
#### Parameters  
 `riid`  
 The IID of the interface pointer that should be returned in `ppUnkSite`.  
  
 `ppUnkSite`  
 Address of the pointer variable that receives the interface pointer requested in `riid`.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 If the site supports the interface requested in `riid`, the pointer is returned by means of `ppUnkSite`. Otherwise, `ppUnkSite` is set to NULL.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)