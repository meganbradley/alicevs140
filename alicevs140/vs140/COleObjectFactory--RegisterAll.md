---
title: "COleObjectFactory::RegisterAll"
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
ms.assetid: afd341e0-18df-43b6-a6fd-fc6edef0f1da
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::RegisterAll
Registers all of the application's object factories with the OLE system DLLs.  
  
## Syntax  
  
```  
  
static BOOL PASCAL RegisterAll( );  
```  
  
## Return Value  
 Nonzero if the factories are successfully registered; otherwise 0.  
  
## Remarks  
 This function is usually called by [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md) when the application is launched.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleObjectFactory::Revoke](../vs140/COleObjectFactory--Revoke.md)   
 [COleObjectFactory::Register](../vs140/COleObjectFactory--Register.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)