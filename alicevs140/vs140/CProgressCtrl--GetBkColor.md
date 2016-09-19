---
title: "CProgressCtrl::GetBkColor"
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
ms.assetid: 5a3c547b-1a34-4e0d-9880-b8eeb85423a9
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CProgressCtrl::GetBkColor
Gets the background color of the current progress bar.  
  
## Syntax  
  
```  
COLORREF GetBkColor() const;  
```  
  
## Return Value  
 The background color of the current progress bar, represented as a [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value.  
  
## Remarks  
 This method sends the [PBM_GETBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760828) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CProgressCtrl Class](../vs140/CProgressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PBM_GETBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760828)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)   
 [Using CProgressCtrl](../vs140/Using-CProgressCtrl.md)   
 [CProgressCtrl::SetBkColor](../vs140/CProgressCtrl--SetBkColor.md)