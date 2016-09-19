---
title: "CMFCToolBarsCustomizeDialog::OnAssignKey"
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
ms.assetid: 43d42034-6ae8-437e-bedc-f458e44b0bd0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::OnAssignKey
Validates keyboard shortcuts as a user defines them.  
  
## Syntax  
  
```  
virtual BOOL OnAssignKey(  
   ACCEL* pAccel   
);  
```  
  
#### Parameters  
 [in, out] `pAccel`  
 Pointer to the proposed keyboard assigment that is expressed as an [ACCEL](http://msdn.microsoft.com/library/windows/desktop/ms646340) struct.  
  
## Return Value  
 `TRUE` if the key can be assigned, or `FALSE` if the key cannot be assigned. The default implementation always returns `TRUE`.  
  
## Remarks  
 Override this method in a derived class to perform extra processing when a user assigns a new keyboard shortcut, or to validate keyboard shortcuts as the user defines them. To prevent a shortcut from being assigned, return `FALSE`. You should also display a message box or otherwise inform the user of the reason why the keyboard shortcut was rejected.  
  
## Requirements  
 **Header:** afxToolBarsCustomizeDialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)