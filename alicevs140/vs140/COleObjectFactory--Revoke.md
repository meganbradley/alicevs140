---
title: "COleObjectFactory::Revoke"
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
ms.assetid: d8c01c0a-4e60-42ee-b8a6-a728cff48afa
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::Revoke
Revokes this object factory's registration with the OLE system DLLs.  
  
## Syntax  
  
```  
  
void Revoke( );  
```  
  
## Remarks  
 The framework calls this function automatically before the application terminates. If necessary, call it from an override of [CWinApp::ExitInstance](../vs140/CWinApp--ExitInstance.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleObjectFactory::RevokeAll](../vs140/COleObjectFactory--RevokeAll.md)   
 [COleObjectFactory::Register](../vs140/COleObjectFactory--Register.md)   
 [CWinApp::ExitInstance](../vs140/CWinApp--ExitInstance.md)