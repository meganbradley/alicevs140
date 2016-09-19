---
title: "CMFCDropDownToolbarButton::OnDrawOnCustomizeList"
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
ms.assetid: 460fcd1e-a5e0-49fd-bf3b-1a2eb817be49
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::OnDrawOnCustomizeList
Called by the framework to draw the button in the **Commands** pane of the **Customize** dialog box.  
  
## Syntax  
  
```  
virtual int OnDrawOnCustomizeList(  
   CDC* pDC,  
   const CRect& rect,  
   BOOL bSelected  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 The device context that displays the button.  
  
 [in] `rect`  
 The bounding rectangle of the button.  
  
 [in] `bSelected`  
 Whether the button is selected. If this parameter is `TRUE`, the button is selected. If this parameter is `FALSE`, the button is not selected.  
  
## Return Value  
 The width, in pixels, of the button on the specified device context.  
  
## Remarks  
 This method is called by the customization dialog box (**Commands** tab) when the button is required to display itself on the owner-draw list box.  
  
 This method extends the base class implementation ([CMFCToolBarButton::OnDrawOnCustomizeList](../vs140/CMFCToolBarButton--OnDrawOnCustomizeList.md)) by changing the text label of the button to the name of the button (that is,to the value of the `lpszName` parameter that you passed to the constructor).  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnDrawOnCustomizeList](../vs140/CMFCToolBarButton--OnDrawOnCustomizeList.md)   
 [CMFCDropDownToolbarButton::CMFCDropDownToolbarButton](../vs140/CMFCDropDownToolbarButton--CMFCDropDownToolbarButton.md)