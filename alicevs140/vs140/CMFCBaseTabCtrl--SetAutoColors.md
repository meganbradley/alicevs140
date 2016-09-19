---
title: "CMFCBaseTabCtrl::SetAutoColors"
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
ms.assetid: 0d69079f-c358-4e8f-a742-bca7074a1877
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::SetAutoColors
Sets the colors of the tab control that the framework uses in automatic color mode.  
  
## Syntax  
  
```  
void SetAutoColors(  
   const CArray<COLORREF,COLORREF>& arColors   
);  
```  
  
#### Parameters  
 [in] `arColors`  
 An array of RGB colors.  
  
## Remarks  
 If you provide a custom array of colors, the default array of colors is ignored. If the parameter `arColors` is empty, the framework reverts to the default array of colors.  
  
 To enable autocolor mode, use the [CMFCBaseTabCtrl::EnableAutoColor](../vs140/CMFCBaseTabCtrl--EnableAutoColor.md) method.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::EnableAutoColor](../vs140/CMFCBaseTabCtrl--EnableAutoColor.md)