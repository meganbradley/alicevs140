---
title: "COleChangeSourceDialog::COleChangeSourceDialog"
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
ms.assetid: b52046b3-4d99-48bb-8bdd-3486989ab874
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleChangeSourceDialog::COleChangeSourceDialog
This function constructs a `COleChangeSourceDialog` object.  
  
## Syntax  
  
```  
  
      explicit COleChangeSourceDialog(  
   COleClientItem* pItem,  
   CWnd* pParentWnd = NULL   
);  
```  
  
#### Parameters  
 `pItem`  
 Pointer to the linked [COleClientItem](../vs140/COleClientItem-Class.md) whose source is to be updated.  
  
 `pParentWnd`  
 Points to the parent or owner window object (of type `CWnd`) to which the dialog object belongs. If it is **NULL**, the parent window of the dialog box will be set to the main application window.  
  
## Remarks  
 To display the dialog box, call the [DoModal](../vs140/COleChangeSourceDialog--DoModal.md) function.  
  
 For more information, see the [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure and [OleUIChangeSource](http://msdn.microsoft.com/library/windows/desktop/ms682497) function in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleChangeSourceDialog Class](../vs140/COleChangeSourceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)