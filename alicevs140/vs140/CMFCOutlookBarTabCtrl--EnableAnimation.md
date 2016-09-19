---
title: "CMFCOutlookBarTabCtrl::EnableAnimation"
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
ms.assetid: 05fe8a9e-4c2b-4113-91bc-4a02a6a3b9db
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarTabCtrl::EnableAnimation
Specifies whether the animation that occurs during the switch between active tabs is enabled.  
  
## Syntax  
  
```  
static void EnableAnimation(  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 Specifies whether the animation should be enabled or disabled.  
  
## Remarks  
 Call this function to enable and disable animation. When the user opens a tab page, the page's caption slides up or down if animation is enabled. If animation is disabled, the page becomes active immediately.  
  
 By the default, the animation is enabled.  
  
## Requirements  
 **Header:** afxOutlookBarTabCtrl.h  
  
## See Also  
 [CMFCOutlookBarTabCtrl Class](../vs140/CMFCOutlookBarTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)