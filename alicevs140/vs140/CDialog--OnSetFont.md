---
title: "CDialog::OnSetFont"
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
ms.assetid: bee88a27-9e50-4de2-abc5-e431154ca218
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::OnSetFont
Specifies the font a dialog-box control will use when drawing text.  
  
## Syntax  
  
```  
Virtual void OnSetFont(  
   CFont* pFont   
);  
```  
  
#### Parameters  
 [in] `pFont`  
 Specifies a pointer to the font that will be used as the default font for all controls in this dialog box.  
  
## Remarks  
 The dialog box will use the specified font as the default for all its controls.  
  
 The dialog editor typically sets the dialog-box font as part of the dialog-box template resource.  
  
> [!NOTE]
>  You cannot override this method when you use a `CFileDialog` object in a program that is compiled under [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)]. For more information about changes to `CFileDialog` under [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)] see [CFileDialog Class](../vs140/CFileDialog-Class.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_SETFONT](http://msdn.microsoft.com/library/windows/desktop/ms632642)   
 [CWnd::SetFont](../vs140/CWnd--SetFont.md)