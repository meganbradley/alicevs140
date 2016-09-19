---
title: "COleObjectFactory::UpdateRegistry"
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
ms.assetid: 80c46635-590b-40e0-9499-0080bf3f66f1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::UpdateRegistry
Registers all of the application's object factories with the OLE system registry.  
  
## Syntax  
  
```  
  
      void UpdateRegistry(  
   LPCTSTR lpszProgID = NULL   
);  
virtual BOOL UpdateRegistry(   
   BOOL bRegister    
);  
```  
  
#### Parameters  
 `lpszProgID`  
 Pointer to a string containing the human-readable program identifier, such as "Excel.Document.5."  
  
 `bRegister`  
 Determines whether the control class's object factory is to be registered.  
  
## Remarks  
 Brief discussions of the two forms for this function follow:  
  
-   **UpdateRegistry(**  `lpszProgID`  **)** Registers this object factory with the OLE system registry. This function is usually called by [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md) when the application is launched.  
  
-   **UpdateRegistry(**  `bRegister`  **)** This form of the function is overridable. If `bRegister` is **TRUE**, this function registers the control class with the system registry. Otherwise, it unregisters the class.  
  
     If you use MFC ActiveX ControlWizard to create your project, ControlWizard supplies an override to this pure virtual function.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleObjectFactory::Revoke](../vs140/COleObjectFactory--Revoke.md)   
 [COleObjectFactory::Register](../vs140/COleObjectFactory--Register.md)   
 [COleObjectFactory::UpdateRegistryAll](../vs140/COleObjectFactory--UpdateRegistryAll.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)