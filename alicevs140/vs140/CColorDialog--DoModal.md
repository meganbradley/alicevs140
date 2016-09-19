---
title: "CColorDialog::DoModal"
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
ms.assetid: f07cf4fa-53b9-44ae-91b6-6863f7f0856b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CColorDialog::DoModal
Call this function to display the Windows common color dialog box and allow the user to select a color.  
  
## Syntax  
  
```  
  
virtual INT_PTR DoModal( );  
```  
  
## Return Value  
 **IDOK** or **IDCANCEL**. If **IDCANCEL** is returned, call the Windows [CommDlgExtendedError](http://msdn.microsoft.com/library/windows/desktop/ms646916) function to determine whether an error occurred.  
  
 **IDOK** and **IDCANCEL** are constants that indicate whether the user selected the OK or Cancel button.  
  
## Remarks  
 If you want to initialize the various color dialog-box options by setting members of the [m_cc](../vs140/CColorDialog--m_cc.md) structure, you should do this before calling `DoModal` but after the dialog-box object is constructed.  
  
 After calling `DoModal`, you can call other member functions to retrieve the settings or information input by the user into the dialog box.  
  
## Example  
 See the example for [CColorDialog::CColorDialog](../vs140/CColorDialog--CColorDialog.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CColorDialog Class](../vs140/CColorDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::DoModal](../vs140/CDialog--DoModal.md)   
 [CColorDialog::CColorDialog](../vs140/CColorDialog--CColorDialog.md)