---
title: "CToolTipCtrl::Popup"
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
ms.assetid: 6cab3554-6acd-4476-81a3-2001e48ee6ec
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::Popup
Causes the current tooltip control to display at the coordinates of the last mouse message.  
  
## Syntax  
  
```  
void Popup();  
```  
  
## Remarks  
 This method sends the [TTM_POPUP](http://msdn.microsoft.com/library/windows/desktop/bb760402) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in Windows XP and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example displays a tooltip window.  
  
 [!CODE [NVC_MFC_CToolBarCtrl_s1#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CToolbarCtrl_s1#7)]  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TTM_POPUP](http://msdn.microsoft.com/library/windows/desktop/bb760402)