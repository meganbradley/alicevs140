---
title: "CToolTipCtrl::SetDelayTime"
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
ms.assetid: 269deb38-c0f9-4416-86c7-115ebd4852e4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::SetDelayTime
Sets the delay time for a tool tip control.  
  
## Syntax  
  
```  
  
      void SetDelayTime(  
   UINT nDelay   
);  
void SetDelayTime(  
   DWORD dwDuration,  
   int iTime   
);  
```  
  
#### Parameters  
 *nDelay*  
 Specifies the new delay time, in milliseconds.  
  
 `dwDuration`  
 Flag that specifies which duration value will be retrieved. See [CToolTipCtrl::GetDelayTime](../vs140/CToolTipCtrl--GetDelayTime.md) for a description of the valid values.  
  
 *iTime*  
 The specified delay time, in milliseconds.  
  
## Remarks  
 The delay time is the length of time the cursor must remain on a tool before the tool tip window appears. The default delay time is 500 milliseconds.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::Activate](../vs140/CToolTipCtrl--Activate.md)   
 [CToolTipCtrl::HitTest](../vs140/CToolTipCtrl--HitTest.md)   
 [CToolTipCtrl::GetDelayTime](../vs140/CToolTipCtrl--GetDelayTime.md)   
 [TTM_SETDELAYTIME](http://msdn.microsoft.com/library/windows/desktop/bb760404)