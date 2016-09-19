---
title: "CMDIFrameWndEx::EnableMDITabs"
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
ms.assetid: 0cb3459e-a138-4268-b0a9-8b64fcaa1a93
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::EnableMDITabs
Enables or disables the MDI Tabs feature for the MDI frame window. When enabled, the frame window displays a tab for each MDI child window.  
  
## Syntax  
  
```  
void EnableMDITabs(  
   BOOL bEnable=TRUE,  
   BOOL bIcons=TRUE,  
   CMFCTabCtrl::Location tabLocation=CMFCTabCtrl::LOCATION_BOTTOM,  
   BOOL bTabCloseButton=FALSE,  
   CMFCTabCtrl::Style style=CMFCTabCtrl::STYLE_3D_SCROLLED,  
   BOOL bTabCustomTooltips=FALSE,  
   BOOL bActiveTabCloseButton=FALSE   
);  
```  
  
#### Parameters  
 `bEnable`  
 Specifies whether tabs are enabled.  
  
 `bIcons`  
 Specifies whether icons should be displayed on the tabs.  
  
 `tabLocation`  
 Specifies the location of the tab labels.  
  
 `bTabCloseButton`  
 Specifies whether to display tab close buttons.  
  
 `style`  
 Specifies the style of tabs. Use `STYLE_3D_SCROLLED` for regular tabs or `STYLE_3D_ONENOTE` for Microsoft OneNote tabs.  
  
 `bTabCustomTooltips`  
 Specifies whether custom tooltips are enabled.  
  
 `bActiveTabCloseButton`  
 If `TRUE`, a **Close** button will be displayed on the active tab instead of on the right corner of the tab area.  
  
## Remarks  
 Call this method to enable or disable the MDI tabs feature for the MDI frame window. When enabled, all child windows are displayed as tabs.  
  
 The tab labels can be located at the top or bottom of the frame, depending on the setting of the parameter `tabLocation`. You may specify either `CMFCTabCtrl::LOCATION_BOTTOM` (the default setting) or `CMFCTabCtrl::LOCATION_TOP`.  
  
 If `bTabCustomTooltips` is `TRUE`, an `AFX_WM_ON_GET_TAB_TOOLTIP` message will be sent to the main frame window. Your code can handle this message and provide the framework with custom tooltips for MDI tabs.  
  
## Example  
 The following example shows how `EnableMDITabs` is used in the [MDITabsDemo Sample: MFC Tabbed MDI Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_MDITabsDemo#3](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_MDITabsDemo#3)]  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)