---
title: "CTabbedPane::SetTabAutoColors"
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
ms.assetid: f932c14a-3a09-4b0c-a936-82ab2f106eea
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabbedPane::SetTabAutoColors
Sets a list of custom colors that are used when the auto color feature is enabled.  
  
## Syntax  
  
```  
static void SetTabAutoColors(  
    const CArray<COLORREF, COLORREF>& arColors  
);  
```  
  
#### Parameters  
 [in] `arColors`  
 Contains the array of colors to set.  
  
## Remarks  
 Use this method to customize the list of colors that are used when the auto color feature is enabled. This is a static function and affects all tabbed panes in your application.  
  
 Use [CTabbedPane::EnableTabAutoColor](../vs140/CTabbedPane--EnableTabAutoColor.md) to enable or disable the auto color feature.  
  
## Requirements  
 **Header:** afxTabbedPane.h  
  
## See Also  
 [CTabbedPane Class](../vs140/CTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)