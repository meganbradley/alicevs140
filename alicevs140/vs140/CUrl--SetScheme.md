---
title: "CUrl::SetScheme"
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
ms.assetid: c9221f33-fa0e-43e7-8f22-c5e2de140c70
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::SetScheme
Call this method to set the URL scheme.  
  
## Syntax  
  
```  
  
      inline BOOL SetScheme(  
   ATL_URL_SCHEME nScheme   
) throw( );  
```  
  
#### Parameters  
 `nScheme`  
 One of the [ATL_URL_SCHEME](../vs140/ATL_URL_SCHEME.md) values for the scheme.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Remarks  
 You can also set the scheme by name (see [CUrl::SetSchemeName](../vs140/CUrl--SetSchemeName.md)).  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)   
 [CUrl::GetScheme](../vs140/CUrl--GetScheme.md)