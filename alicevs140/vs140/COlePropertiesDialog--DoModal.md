---
title: "COlePropertiesDialog::DoModal"
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
ms.assetid: b04a2673-70a7-44cd-b5e3-173fc02d423a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertiesDialog::DoModal
Call this member function to display the Windows common OLE Object Properties dialog box and allow the user to view and/or change the various properties of the document item.  
  
## Syntax  
  
```  
  
virtual INT_PTR DoModal( );  
  
```  
  
## Return Value  
 **IDOK** or **IDCANCEL** if successful; otherwise 0. **IDOK** and **IDCANCEL** are constants that indicate whether the user selected the OK or Cancel button.  
  
 If **IDCANCEL** is returned, you can call the Windows [CommDlgExtendedError](http://msdn.microsoft.com/library/windows/desktop/ms646916) function to determine whether an error occurred.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePropertiesDialog Class](../vs140/COlePropertiesDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePropertiesDialog::OnApplyScale](../vs140/COlePropertiesDialog--OnApplyScale.md)   
 [COlePropertiesDialog::m_psh](../vs140/COlePropertiesDialog--m_psh.md)