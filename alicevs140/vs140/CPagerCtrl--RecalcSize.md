---
title: "CPagerCtrl::RecalcSize"
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
ms.assetid: 5875647e-e2ca-43d3-b27a-7dba3b0d3011
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::RecalcSize
Causes the current pager control to recalculate the size of the contained window.  
  
## Syntax  
  
```  
void RecalcSize();  
```  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Remarks  
 This method sends the [PGM_RECALCSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760876) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. Consequently, the pager control sends the [PGN_CALCSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760864) notification to obtain the scrollable dimensions of the contained window.  
  
## Example  
 The following example uses the [CPagerCtrl::RecalcSize](../vs140/CPagerCtrl--RecalcSize.md) method to request the current pager control to recalculate its size.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#3)]  
  
## Example  
 The following example uses [message reflection](../vs140/TN062--Message-Reflection-for-Windows-Controls.md) to enable the pager control to recalculate its own size instead of requiring the control's parent dialog to perform the calculation. The example derives the `MyPagerCtrl` class from the [CPagerCtrl class](../vs140/CPagerCtrl-Class.md), then uses a message map to associate the [PGN_CALCSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760864) notification with the `OnCalcsize` notification handler. In this example, the notification handler sets the width and height of the pager control to fixed values.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#8)]  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PGM_RECALCSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760876)   
 [PGN_CALCSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760864)