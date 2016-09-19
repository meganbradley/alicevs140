---
title: "CMFCToolBarsCustomizeDialog::OnEditToolbarMenuImage"
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
ms.assetid: 8e2d3cfe-4ee0-4bb9-ad91-89fbd78f5acf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::OnEditToolbarMenuImage
Starts an image editor so that a user can customize a toolbar button or menu item icon.  
  
## Syntax  
  
```  
virtual BOOL OnEditToolbarMenuImage(  
   CWnd* pWndParent,  
   CBitmap& bitmap,  
   int nBitsPerPixel   
);  
```  
  
#### Parameters  
 [in] `pWndParent`  
 A pointer to the parent window.  
  
 [in] `bitmap`  
 A reference to a bitmap object to be edited.  
  
 [in] `nBitsPerPixel`  
 Bitmap color resolution, in bits per pixel.  
  
## Return Value  
 `TRUE` if a change is being committed; otherwise `FALSE`. The default implementation displays a dialog box and returns `TRUE` if the user clicks **OK**, or `FALSE` if the user clicks **Cancel** or the **Close** button.  
  
## Remarks  
 This method is called by the framework when the user runs the image editor. The default implementation displays [CMFCImageEditorDialog Class](../vs140/CMFCImageEditorDialog-Class.md) dialog box. Override `OnEditToolbarMenuImage` in a derived class to use a custom image editor.  
  
## Requirements  
 **Header:** afxToolBarsCustomizeDialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)