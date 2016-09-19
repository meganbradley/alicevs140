---
title: "CFindReplaceDialog::Create"
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
ms.assetid: ef346e81-bdd3-4f3e-8651-8b2145f201b8
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFindReplaceDialog::Create
Creates and displays either a Find or Find/Replace dialog box object, depending on the value of `bFindDialogOnly`.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   BOOL bFindDialogOnly,  
   LPCTSTR lpszFindWhat,  
   LPCTSTR lpszReplaceWith = NULL,  
   DWORD dwFlags = FR_DOWN,  
   CWnd* pParentWnd = NULL   
);  
```  
  
#### Parameters  
 `bFindDialogOnly`  
 Set this parameter to `TRUE` to display a **Find** dialog box. Set it to `FALSE` to display a **Find/Replace** dialog box.  
  
 `lpszFindWhat`  
 Pointer to the default search string when the dialog box appears. If `NULL`, the dialog box does not contain a default search string.  
  
 `lpszReplaceWith`  
 Pointer to the default replacement string when the dialog box appears. If `NULL`, the dialog box does not contain a default replacement string.  
  
 `dwFlags`  
 One or more flags you can use to customize the settings of the dialog box, combined using the bitwise OR operator. The default value is `FR_DOWN`, which specifies that the search is to proceed in a downward direction. See the [FINDREPLACE](http://msdn.microsoft.com/library/windows/desktop/ms646835) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information on these flags.  
  
 `pParentWnd`  
 A pointer to the dialog box's parent or owner window. This is the window that will receive the special message indicating that a find/replace action is requested. If `NULL`, the main window of the application is used.  
  
## Return Value  
 Nonzero if the dialog box object was successfully created; otherwise 0.  
  
## Remarks  
 In order for the parent window to be notified of find/replace requests, you must use the Windows [RegisterWindowMessage](http://msdn.microsoft.com/library/windows/desktop/ms644947) function whose return value is a message number unique to the application's instance. Your frame window should have a message map entry that declares the callback function (`OnFindReplace` in the example that follows) that handles this registered message. The following code fragment is an example of how to do this for a frame window class named `CMyRichEditView`:  
  
 [!CODE [NVC_MFCDocView#171](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#171)]  
  
 [!CODE [NVC_MFCDocView#172](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#172)]  
  
 [!CODE [NVC_MFCDocView#173](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#173)]  
  
 Within your `OnFindReplace` function, you interpret the intentions of the user by using the [FindNext](../vs140/CFindReplaceDialog--FindNext.md) and [IsTerminating](../vs140/CFindReplaceDialog--IsTerminating.md) methods and you create the code for the find/replace operations.  
  
## Example  
 See the example for [CFindReplaceDialog::CFindReplaceDialog](../vs140/CFindReplaceDialog--CFindReplaceDialog.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFindReplaceDialog Class](../vs140/CFindReplaceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFindReplaceDialog::CFindReplaceDialog](../vs140/CFindReplaceDialog--CFindReplaceDialog.md)