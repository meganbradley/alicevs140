---
title: "CAtlExeModuleT::PostMessageLoop"
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
ms.assetid: 8badf726-ad2a-41c4-8b8c-5c52fb7c7fc3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlExeModuleT::PostMessageLoop
This method is called immediately after the message loop exits.  
  
## Syntax  
  
```  
  
HRESULT PostMessageLoop( ) throw( );  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 Override this method to perform custom application cleanup. The default implementation calls [CAtlExeModuleT::RevokeClassObjects](../vs140/CAtlExeModuleT--RevokeClassObjects.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlExeModuleT Class](../vs140/CAtlExeModuleT-Class.md)   
 [CAtlExeModuleT::PreMessageLoop](../vs140/CAtlExeModuleT--PreMessageLoop.md)