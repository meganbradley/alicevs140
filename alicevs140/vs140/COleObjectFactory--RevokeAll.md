---
title: "COleObjectFactory::RevokeAll"
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
ms.assetid: a2b44a51-a65d-4572-a90a-d46987c8ab95
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::RevokeAll
Revokes all of the application's object factories' registrations with the OLE system DLLs.  
  
## Syntax  
  
```  
  
static void PASCAL RevokeAll( );  
```  
  
## Remarks  
 The framework calls this function automatically before the application terminates. If necessary, call it from an override of [CWinApp::ExitInstance](../vs140/CWinApp--ExitInstance.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleObjectFactory::Revoke](../vs140/COleObjectFactory--Revoke.md)   
 [COleObjectFactory::Register](../vs140/COleObjectFactory--Register.md)   
 [CWinApp::ExitInstance](../vs140/CWinApp--ExitInstance.md)