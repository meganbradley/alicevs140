---
title: "CTaskDialog::ClickCommandControl"
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
ms.assetid: c452e204-4222-4f31-816f-352b59f21d60
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::ClickCommandControl
Clicks a command button control or common button programmatically.  
  
## Syntax  
  
```  
protected:  
void ClickCommandControl(  
   int nCommandControlID  
) const;  
```  
  
#### Parameters  
 [in] `nCommandControlID`  
 The command ID of the control to click.  
  
## Remarks  
 This method generates the windows message `TDM_CLICK_BUTTON`.  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::ClickRadioButton](../vs140/CTaskDialog--ClickRadioButton.md)