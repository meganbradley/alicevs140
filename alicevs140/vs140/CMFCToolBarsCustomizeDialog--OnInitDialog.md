---
title: "CMFCToolBarsCustomizeDialog::OnInitDialog"
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
ms.assetid: 8772d1cc-9b4d-4f8f-a961-b528dde12027
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::OnInitDialog
Overrides to augment property sheet initialization.  
  
## Syntax  
  
```  
virtual BOOL OnInitDialog();  
```  
  
## Return Value  
 The result of calling the [CPropertySheet::OnInitDialog](../vs140/CPropertySheet--OnInitDialog.md) method.  
  
## Remarks  
 This method extends the base class implementation, [CPropertySheet::OnInitDialog](../vs140/CPropertySheet--OnInitDialog.md), by displaying the **Close** button, by making sure that the dialog box fits the current screen size, and by moving the **Help** button to the lower-left corner of the dialog box.  
  
## Requirements  
 **Header:** afxtoolbarscustomizedialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::OnInitDialog](../vs140/CPropertySheet--OnInitDialog.md)