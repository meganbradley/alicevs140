---
title: "CUrl::SetPortNumber"
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
ms.assetid: 312b708c-687f-4525-bc31-40aaf827e64e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::SetPortNumber
Call this method to set the port number.  
  
## Syntax  
  
```  
  
      inline BOOL SetPortNumber(  
   ATL_URL_PORT nPrt   
) throw( );  
```  
  
#### Parameters  
 *nPrt*  
 The port number.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)   
 [CUrl::GetPortNumber](../vs140/CUrl--GetPortNumber.md)   
 [ATL_URL_PORT](../vs140/ATL_URL_PORT.md)