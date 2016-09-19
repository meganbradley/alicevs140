---
title: "COleObjectFactory::UpdateRegistryAll"
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
ms.assetid: 60adcf43-f9f7-45ee-a09d-df9ccc6e1c77
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::UpdateRegistryAll
Registers all of the application's object factories with the OLE system registry.  
  
## Syntax  
  
```  
  
      static BOOL PASCAL UpdateRegistryAll(  
   BOOL bRegister = TRUE  
);  
```  
  
#### Parameters  
 `bRegister`  
 Determines whether the control class's object factory is to be registered.  
  
## Return Value  
 Nonzero if the factories are successfully updated; otherwise 0.  
  
## Remarks  
 This function is usually called by [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md) when the application is launched.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleObjectFactory::Revoke](../vs140/COleObjectFactory--Revoke.md)   
 [COleObjectFactory::Register](../vs140/COleObjectFactory--Register.md)   
 [COleObjectFactory::UpdateRegistry](../vs140/COleObjectFactory--UpdateRegistry.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)