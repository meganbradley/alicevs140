---
title: "CCmdUI::SetCheck"
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
ms.assetid: 74e103a7-5a7f-4e1b-a4c8-beaed5356d6a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdUI::SetCheck
Call this member function to set the user-interface item for this command to the appropriate check state.  
  
## Syntax  
  
```  
  
      virtual void SetCheck(  
   int nCheck = 1   
);  
```  
  
#### Parameters  
 `nCheck`  
 Specifies the check state to set. If 0, unchecks; if 1, checks; and if 2, sets indeterminate.  
  
## Remarks  
 This member function works for menu items and toolbar buttons. The indeterminate state applies only to toolbar buttons.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdUI Class](../vs140/CCmdUI-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdUI::SetRadio](../vs140/CCmdUI--SetRadio.md)