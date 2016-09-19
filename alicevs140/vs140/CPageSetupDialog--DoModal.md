---
title: "CPageSetupDialog::DoModal"
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
ms.assetid: 09a99693-2870-413d-b316-3e7254244453
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPageSetupDialog::DoModal
Call this function to display the Windows common OLE Page Setup dialog box and allow the user to select various print setup options such as the printing margins, size and orientation of the paper, and destination printer.  
  
## Syntax  
  
```  
  
virtual INT_PTR DoModal( );  
  
```  
  
## Return Value  
 **IDOK** or **IDCANCEL**. If **IDCANCEL** is returned, call the Windows [CommDlgExtendedError](http://msdn.microsoft.com/library/windows/desktop/ms646916) function to determine whether an error occurred.  
  
 **IDOK** and **IDCANCEL** are constants that indicate whether the user selected the OK or Cancel button.  
  
## Remarks  
 In addition, the user can access the printer setup options such as network location and properties specific to the selected printer.  
  
 If you want to initialize the various Page Setup dialog options by setting members of the `m_psd` structure, you should do so before calling `DoModal`, and after the dialog object is constructed. After calling `DoModal`, call other member functions to retrieve the settings or information input by the user into the dialog box.  
  
 If you want to propagate the current settings entered by the user, make a call to [CWinApp::SelectPrinter](../vs140/CWinApp--SelectPrinter.md). This function takes the information from the `CPageSetupDialog` object and initializes and selects a new printer DC with the proper attributes.  
  
 [!CODE [NVC_MFCDocView#95](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#95)]  
  
## Example  
 See the example for [CPageSetupDialog::CPageSetupDialog](../vs140/CPageSetupDialog--CPageSetupDialog.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPageSetupDialog Class](../vs140/CPageSetupDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPageSetupDialog::m_psd](../vs140/CPageSetupDialog--m_psd.md)