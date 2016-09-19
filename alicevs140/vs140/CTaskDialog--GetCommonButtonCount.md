---
title: "CTaskDialog::GetCommonButtonCount"
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
ms.assetid: 9b2249e9-ee76-48b5-a49c-95d33a1092e3
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::GetCommonButtonCount
Retrieves the number of common buttons.  
  
## Syntax  
  
```  
int GetCommonButtonCount() const;  
```  
  
## Return Value  
 The number of common buttons available.  
  
## Remarks  
 The common buttons are the default buttons that you provide to [CTaskDialog::CTaskDialog](../vs140/CTaskDialog--CTaskDialog.md). The [CTaskDialog Class](../vs140/CTaskDialog-Class.md) displays the buttons along the bottom of the dialog box.  
  
 The enumerated list of buttons is provided in CommCtrl.h.  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::GetCommonButtonFlag](../vs140/CTaskDialog--GetCommonButtonFlag.md)   
 [CTaskDialog::GetCommonButtonId](../vs140/CTaskDialog--GetCommonButtonId.md)