---
title: "CProgressCtrl::GetBarColor"
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
ms.assetid: 13d44072-058a-403e-bc9e-a9d087c9c491
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CProgressCtrl::GetBarColor
Gets the color of the progress indicator bar for the current progress bar control.  
  
## Syntax  
  
```  
COLORREF GetBarColor() const;  
```  
  
## Return Value  
 The color of the current progress bar, represented as a [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value, or `CLR_DEFAULT` if the progress indicator bar color is the default color.  
  
## Remarks  
 This method sends the [PBM_GETBARCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760826) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CProgressCtrl Class](../vs140/CProgressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PBM_GETBARCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760826)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)   
 [Using CProgressCtrl](../vs140/Using-CProgressCtrl.md)   
 [CProgressCtrl::SetBarColor](../vs140/CProgressCtrl--SetBarColor.md)