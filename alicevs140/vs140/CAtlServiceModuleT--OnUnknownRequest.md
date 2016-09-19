---
title: "CAtlServiceModuleT::OnUnknownRequest"
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
ms.assetid: fc1ce76a-0f07-4beb-8272-bac3eaa4920b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::OnUnknownRequest
Override this method to handle unknown requests to the service.  
  
## Syntax  
  
```  
  
      void OnUnknownRequest(  
   DWORD /* dwOpcode */  
) throw( );  
```  
  
#### Parameters  
 */\* dwOpcode \*/*  
 Reserved.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlServiceModuleT Class](../vs140/CAtlServiceModuleT-Class.md)   
 [CAtlServiceModuleT::Handler](../vs140/CAtlServiceModuleT--Handler.md)