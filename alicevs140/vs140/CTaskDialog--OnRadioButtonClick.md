---
title: "CTaskDialog::OnRadioButtonClick"
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
ms.assetid: 67b7dd41-cf18-4781-a784-8ab8327ea75d
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::OnRadioButtonClick
The framework calls this method when the user selects a radio button control.  
  
## Syntax  
  
```  
virtual HRESULT OnRadioButtonClick(  
   int nRadioButtonID  
);  
```  
  
#### Parameters  
 [in] `nRadioButtonID`  
 The ID of the radio button control that the user clicked.  
  
## Return Value  
 The default implementation returns `S_OK`.  
  
## Remarks  
 Override this method in a derived class to implement custom behavior.  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::TaskDialogCallback](../vs140/CTaskDialog--TaskDialogCallback.md)