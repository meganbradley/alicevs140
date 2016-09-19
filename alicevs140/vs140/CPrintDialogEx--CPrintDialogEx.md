---
title: "CPrintDialogEx::CPrintDialogEx"
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
ms.assetid: 2e1e4401-4377-4c92-b5b6-5710acf21999
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::CPrintDialogEx
Constructs a Windows 2000 Print property sheet.  
  
## Syntax  
  
```  
  
      CPrintDialogEx(  
   DWORD dwFlags = PD_ALLPAGES | PD_USEDEVMODECOPIES | PD_NOPAGENUMS  
      | PD_HIDEPRINTTOFILE | PD_NOSELECTION | PD_NOCURRENTPAGE,  
   CWnd* pParentWnd = NULL  
);  
```  
  
#### Parameters  
 `dwFlags`  
 One or more flags you can use to customize the settings of the dialog box, combined using the bitwise OR operator. For example, the **PD_ALLPAGES** flag sets the default print range to all pages of the document. See the [PRINTDLGEX](http://msdn.microsoft.com/library/windows/desktop/ms646844) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information on these flags.  
  
 `pParentWnd`  
 A pointer to the dialog box's parent or owner window.  
  
## Remarks  
 This member function only constructs the object. Use the `DoModal` member function to display the dialog box.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::DoModal](../vs140/CPrintDialogEx--DoModal.md)   
 [Print Property Sheet](http://msdn.microsoft.com/library/windows/desktop/ms646966)