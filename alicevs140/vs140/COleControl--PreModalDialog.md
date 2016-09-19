---
title: "COleControl::PreModalDialog"
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
ms.assetid: ba73629e-a4a9-41fd-a9e6-89ae37ee19dd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::PreModalDialog
Notifies the container that a modal dialog box is about to be displayed.  
  
## Syntax  
  
```  
  
      void PreModalDialog(  
   HWND hWndParent = NULL  
);  
```  
  
#### Parameters  
 `hWndParent`  
 Handle to the parent window of the modal dialog box.  
  
## Remarks  
 Call this function before displaying any modal dialog box. You must call this function so that the container can disable all its top-level windows. After the modal dialog box has been displayed, you must then call `PostModalDialog`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::PostModalDialog](../vs140/COleControl--PostModalDialog.md)