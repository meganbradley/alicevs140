---
title: "COlePropertyPage::OnInitDialog"
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
ms.assetid: 21a8a768-281c-4e9b-9175-b868fdd6aa9c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::OnInitDialog
The framework calls this function when the property page's dialog is initialized.  
  
## Syntax  
  
```  
  
virtual BOOL OnInitDialog( );  
```  
  
## Return Value  
 The default implementation returns **FALSE**.  
  
## Remarks  
 Override it if any special action is required when the dialog is initialized. The default implementation calls `CDialog::OnInitDialog` and returns **FALSE**.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::OnInitDialog](../vs140/CDialog--OnInitDialog.md)