---
title: "CMFCToolBar::SetToolBarBtnText"
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
ms.assetid: ac59f487-1db5-4502-b6df-5379903c6045
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetToolBarBtnText
Specifies properties of a button on the toolbar.  
  
## Syntax  
  
```  
void SetToolBarBtnText(  
   UINT nBtnIndex,  
   LPCTSTR szText=NULL,  
   BOOL bShowText=TRUE,  
   BOOL bShowImage=TRUE   
);  
```  
  
#### Parameters  
 [in] `nBtnIndex`  
 The zero-based index of the toolbar button in the list of toolbar buttons.  
  
 [in] `szText`  
 Specifies the text label of the toolbar button.  
  
 [in] `bShowText`  
 If this parameter is `TRUE`, the framework shows the text label. Otherwise, the framework hides the text label.  
  
 [in] `bShowImage`  
 If this parameter is `TRUE`, the framework shows the toolbar button image. Otherwise, the framework hides the toolbar button image.  
  
## Remarks  
 By default, the framework shows the images of toolbar buttons but does not show the text label of toolbar buttons.  
  
 In Debug builds, this method generates an assertion failure if `nBtnIndex` does not refer to a valid toolbar button or the toolbar button is a separator.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)