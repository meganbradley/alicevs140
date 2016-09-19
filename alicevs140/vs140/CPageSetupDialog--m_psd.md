---
title: "CPageSetupDialog::m_psd"
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
ms.assetid: e3704958-251b-4979-8f58-7a61ba3df4f2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPageSetupDialog::m_psd
A structure of type **PAGESETUPDLG**, whose members store the characteristics of the dialog object.  
  
## Syntax  
  
```  
  
PAGESETUPDLG m_psd;  
  
```  
  
## Remarks  
 After constructing a `CPageSetupDialog` object, you can use `m_psd` to set various aspects of the dialog box before calling the `DoModal` member function.  
  
 If you modify the `m_psd` data member directly, you will override any default behavior.  
  
 For more information on the [PAGESETUPDLG](http://msdn.microsoft.com/library/windows/desktop/ms646842) structure, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 See the example for [CPageSetupDialog::CPageSetupDialog](../vs140/CPageSetupDialog--CPageSetupDialog.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPageSetupDialog Class](../vs140/CPageSetupDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)