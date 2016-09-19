---
title: "CToolTipCtrl::SetMaxTipWidth"
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
ms.assetid: 947cdc07-9f4f-4626-8a2f-559bf4f5c982
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::SetMaxTipWidth
Sets the maximum width for a tool tip window.  
  
## Syntax  
  
```  
  
      int SetMaxTipWidth(  
   int iWidth   
);  
```  
  
#### Parameters  
 *iWidth*  
 The maximum tool tip window width to be set.  
  
## Return Value  
 The previous maximum tip width.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TTM_SETMAXTIPWIDTH](http://msdn.microsoft.com/library/windows/desktop/bb760408), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::GetMaxTipWidth](../vs140/CToolTipCtrl--GetMaxTipWidth.md)