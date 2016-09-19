---
title: "CReBarCtrl::SetToolTips"
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
ms.assetid: 098b6165-fb9e-4ab1-8ff5-0436d8e46177
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::SetToolTips
Associates a tool tip control with a rebar control.  
  
## Syntax  
  
```  
  
      void SetToolTips(  
   CToolTipCtrl* pToolTip   
);  
```  
  
#### Parameters  
 *pToolTip*  
 A pointer to a [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) object  
  
## Remarks  
 You must destroy the `CToolTipCtrl` object when you are done with it.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::GetToolTips](../vs140/CReBarCtrl--GetToolTips.md)