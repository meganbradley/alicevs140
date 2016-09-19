---
title: "CPrintDialogEx::DoModal"
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
ms.assetid: c1bd61ae-b881-4603-9fb2-0f9e4a7da775
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::DoModal
Call this function to display the Windows 2000 common Print property sheet and allow the user to select various printing options such as the number of copies, page range, and whether copies should be collated.  
  
## Syntax  
  
```  
  
virtual INT_PTR DoModal( );  
  
```  
  
## Return Value  
 The INT_PTR return value is actually an HRESULT. See the Return Values section in [PrintDlgEx](http://msdn.microsoft.com/library/windows/desktop/ms646942) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 If you want to initialize the various print dialog options by setting members of the `m_pdex` structure, you should do this before calling `DoModal`, but after the dialog object is constructed.  
  
 After calling `DoModal`, you can call other member functions to retrieve the settings or information input by the user into the dialog box.  
  
 If the **PD_RETURNDC** flag is used when calling `DoModal`, a printer DC will be returned in the **hDC** member of [m_pdex](../vs140/CPrintDialogEx--m_pdex.md). This DC must be freed with a call to [DeleteDC](http://msdn.microsoft.com/library/windows/desktop/dd183533) by the caller of `CPrintDialogEx`.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::CPrintDialogEx](../vs140/CPrintDialogEx--CPrintDialogEx.md)   
 [CDialog::DoModal](../vs140/CDialog--DoModal.md)