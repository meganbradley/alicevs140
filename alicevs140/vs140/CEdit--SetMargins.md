---
title: "CEdit::SetMargins"
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
ms.assetid: 0e05de4f-4203-42cb-b782-7c7017767046
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::SetMargins
Call this method to set the left and right margins of this edit control.  
  
## Syntax  
  
```  
  
      void SetMargins(  
   UINT nLeft,  
   UINT nRight   
);  
```  
  
#### Parameters  
 *nLeft*  
 The width of the new left margin, in pixels.  
  
 *nRight*  
 The width of the new right margin, in pixels.  
  
## Remarks  
  
> [!NOTE]
>  This member function is available beginning with Windows 95 and Windows NT 4.0.  
  
 For more information, see [EM_SETMARGINS](http://msdn.microsoft.com/library/windows/desktop/bb761649) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CEditView::GetEditCtrl](../vs140/CEditView--GetEditCtrl.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::GetMargins](../vs140/CEdit--GetMargins.md)