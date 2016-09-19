---
title: "CMFCOutlookBarTabCtrl::SetPageButtonTextAlign"
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
ms.assetid: 859be30b-216d-4cf2-9579-960636b6dd8a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarTabCtrl::SetPageButtonTextAlign
Sets the alignment of the text labels on the tab buttons of the Outlook bar.  
  
## Syntax  
  
```  
void SetPageButtonTextAlign(  
   UINT uiAlign,  
   BOOL bRedraw=TRUE   
);  
```  
  
#### Parameters  
 [in] `uiAlign`  
 Specifies the text alignment.  
  
 [in] `bRedraw`  
 If `TRUE`, the outlook window will be redrawn.  
  
## Remarks  
 Use this function to change text alignment for page buttons.  
  
 `uiAlign` can be one of the following values:  
  
|Constant|Meaning|  
|--------------|-------------|  
|TA_LEFT|Left alignment|  
|TA_CENTER|Center alignment|  
|TA_RIGHT|Right alignment|  
  
 The default value is TA_CENTER.  
  
## Requirements  
 **Header:** afxOutlookBarTabCtrl.h  
  
## See Also  
 [CMFCOutlookBarTabCtrl Class](../vs140/CMFCOutlookBarTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)