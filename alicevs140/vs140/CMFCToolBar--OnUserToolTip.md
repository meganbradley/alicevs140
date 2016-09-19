---
title: "CMFCToolBar::OnUserToolTip"
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
ms.assetid: bffb929a-d768-4b4d-94ed-776932045439
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::OnUserToolTip
Called by the framework when the tooltip for a button is about to be displayed.  
  
## Syntax  
  
```  
virtual BOOL OnUserToolTip(  
   CMFCToolBarButton* pButton,  
   CString& strTTText   
) const;  
```  
  
#### Parameters  
 [in] `pButton`  
 Points to a toolbar button for which a tooltip is to be displayed.  
  
 [out] `strTTText`  
 A reference to `CString` object that receives the text of the tooltip.  
  
## Return Value  
 `TRUE` if `strTTText` was populated with tooltip text; otherwise `FALSE`.  
  
## Remarks  
 The framework calls this method when the tooltip for a toolbar button is about to be displayed. If `OnUserToolTip` returns `TRUE`, the framework displays a tooltip which contains the text returned by `OnUserToolTip` in `strTTText`. Otherwise, the tooltip contains the button text.  
  
 Override `OnUserToolTip` to customize tool tips of toolbar buttons. The default implementation calls [CMFCToolBar::OnUserToolTip](../vs140/CMFCToolBar--OnUserToolTip.md) to obtain the tooltip text.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)