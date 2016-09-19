---
title: "CReBarCtrl::GetBandBorders"
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
ms.assetid: 573e63ec-3624-492c-85b2-56c30f060c13
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::GetBandBorders
Implements the behavior of the Win32 message [RB_GETBANDBORDERS](http://msdn.microsoft.com/library/windows/desktop/bb774437), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      void GetBandBorders(  
   UINT uBand,  
   LPRECT prc   
) const;  
```  
  
#### Parameters  
 `uBand`  
 Zero-based index of the band for which the borders will be retrieved.  
  
 `prc`  
 A pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that will receive the band borders. If the rebar control has the **RBS_BANDBORDERS** style, each member of this structure will receive the number of pixels, on the corresponding side of the band, that constitute the border. If the rebar control does not have the **RBS_BANDBORDERS** style, only the left member of this structure receives valid information. For a description of rebar control styles, see [Rebar Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb774377) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)