---
title: "CRichEditCtrl::SetTextMode"
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
ms.assetid: ce90c1a1-4ef1-42d2-932f-28d8d6064e7b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetTextMode
Sets the text mode or undo and redo level for a rich edit control.  
  
## Syntax  
  
```  
  
      BOOL SetTextMode(  
   UINT fMode   
);  
```  
  
#### Parameters  
 *fMode*  
 Specifies the new settings for the control's text mode and undo level parameters. For a list of the possible values, see the mode parameter for [EM_SETTEXTMODE](http://msdn.microsoft.com/library/windows/desktop/bb774286) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Zero if successful, otherwise nonzero.  
  
## Remarks  
 For a description of the text modes, see **EM_SETTEXTMODE** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 This member function fails if the control contains text. To make sure the control is empty, send a [WM_SETTEXT](http://msdn.microsoft.com/library/windows/desktop/ms632644) message with an empty string.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetTextMode](../vs140/CRichEditCtrl--GetTextMode.md)