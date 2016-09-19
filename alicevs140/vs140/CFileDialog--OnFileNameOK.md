---
title: "CFileDialog::OnFileNameOK"
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
ms.assetid: 6e4edbf2-3c60-4850-8b47-7badd42ff1b4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::OnFileNameOK
Override this function only if you want to provide custom validation of filenames that are entered into a common file dialog box.  
  
## Syntax  
  
```  
  
virtual BOOL OnFileNameOK( );  
```  
  
## Return Value  
 1 if the filename is not a valid filename; otherwise 0.  
  
## Remarks  
 This function allows you to reject a filename for any application-specific reason. Normally, you do not need to use this function because the framework provides default validation of filenames and displays a message box if an invalid filename is entered.  
  
 If 1 is returned, the dialog box will remain displayed for the user to enter another filename. The dialog procedure dismisses the dialog if the return is 0. Other nonzero return values are currently reserved and should not be used.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [OPENFILENAME](http://msdn.microsoft.com/library/windows/desktop/ms646839)