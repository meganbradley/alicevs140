---
title: "COleObjectFactory::Register"
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
ms.assetid: 89a573a3-6089-4026-9c64-ae3290676ffb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::Register
Registers this object factory with the OLE system DLLs.  
  
## Syntax  
  
```  
  
virtual BOOL Register( );  
```  
  
## Return Value  
 Nonzero if the factory is successfully registered; otherwise 0.  
  
## Remarks  
 This function is usually called by [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md) when the application is launched.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleObjectFactory::Revoke](../vs140/COleObjectFactory--Revoke.md)   
 [COleObjectFactory::RegisterAll](../vs140/COleObjectFactory--RegisterAll.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)