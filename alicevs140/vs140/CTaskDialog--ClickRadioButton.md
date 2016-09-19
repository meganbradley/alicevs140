---
title: "CTaskDialog::ClickRadioButton"
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
ms.assetid: 149a180a-9bb8-43f4-a10e-298699987a28
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::ClickRadioButton
Clicks a radio button programmatically.  
  
## Syntax  
  
```  
protected:  
void ClickRadioButton(  
   int nRadioButtonID  
) const;  
```  
  
#### Parameters  
 [in] `nRadioButtonID`  
 The ID of the radio button to click.  
  
## Remarks  
 This method generates the windows message `TDM_CLICK_RADIO_BUTTON`.  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::ClickCommandControl](../vs140/CTaskDialog--ClickCommandControl.md)