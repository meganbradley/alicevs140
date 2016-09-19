---
title: "CBindStatusCallback::OnProgress"
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
ms.assetid: ab29a6e8-c65e-4945-895d-46d2b2e55c10
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::OnProgress
Called to indicate the progress of a data downloading process.  
  
## Syntax  
  
```  
  
      STDMETHOD(OnProgress)(  
   ULONG /* ulProgress */,  
   ULONG /* ulProgressMax */,  
   ULONG /* ulStatusCode */,  
   LPCWSTRONG /* szStatusText */   
);  
```  
  
#### Parameters  
 `ulProgress`  
 Unsigned long integer. Unused.  
  
 `ulProgressMax`  
 Unsigned long integer Unused.  
  
 `ulStatusCode`  
 Unsigned long integer. Unused.  
  
 `szStatusText`  
 Address of a string value. Unused.  
  
## Return Value  
 Returns `S_OK`.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)