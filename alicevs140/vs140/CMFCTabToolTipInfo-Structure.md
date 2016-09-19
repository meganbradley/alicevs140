---
title: "CMFCTabToolTipInfo Structure"
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
ms.assetid: 9c3b3fb9-1497-4d59-932b-0da9348dd5e2
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabToolTipInfo Structure
This structure provides information about the MDI tab that the user is hovering over.  
  
## Syntax  
  
```  
struct CMFCTabToolTipInfo  
```  
  
## Members  
  
### Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCTabToolTipInfo::m_nTabIndex;](#cmfctabtooltipinfo__m_ntabindex)|Specifies the index of the tab control.|  
|[CMFCTabToolTipInfo::m_pTabWnd](#cmfctabtooltipinfo__m_ptabwnd)|A pointer to the tab control.|  
|[CMFCTabToolTipInfo::m_strText](#cmfctabtooltipinfo__m_strtext)|The tooltip text.|  
  
## Remarks  
 A pointer to a `CMFCTabToolTipInfo` structure is passed as a parameter of the `AFX_WM_ON_GET_TAB_TOOLTIP` message. This message is generated when MDI tabs are enabled and the user hovers over a tab control.  
  
## Example  
 The following example shows how `CMFCTabToolTipInfo` is used in the [MDITabsDemo Sample: MFC Tabbed MDI Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_MDITabsDemo#2](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_MDITabsDemo#2)]  
  
## Inheritance Hierarchy  
 [CMFCTabToolTipInfo](../vs140/CMFCTabToolTipInfo-Structure.md)  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
##  <a name="cmfctabtooltipinfo__m_ntabindex"></a>  CMFCTabToolTipInfo::m_nTabIndex  
 Specifies the index of the tab control.  
  
```  
int m_nTabIndex;  
```  
  
### Remarks  
 Index of the tab over which the user is hovering.  
  
### Example  
 The following example shows how `m_nTabIndex` is used in the [MDITabsDemo Sample: MFC Tabbed MDI Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_MDITabsDemo#2](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_MDITabsDemo#2)]  
  
##  <a name="cmfctabtooltipinfo__m_ptabwnd"></a>  CMFCTabToolTipInfo::m_pTabWnd  
 A pointer to the tab control.  
  
```  
CMFCBaseTabCtrl* m_pTabWnd;  
```  
  
### Example  
 The following example shows how `m_pTabWnd` is used in the [MDITabsDemo Sample: MFC Tabbed MDI Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_MDITabsDemo#2](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_MDITabsDemo#2)]  
  
##  <a name="cmfctabtooltipinfo__m_strtext"></a>  CMFCTabToolTipInfo::m_strText  
 The tooltip text.  
  
```  
CString m_strText;  
```  
  
### Remarks  
 If the string is empty, the tooltip is not displayed.  
  
### Example  
 The following example shows how `m_strText` is used in the [MDITabsDemo Sample: MFC Tabbed MDI Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_MDITabsDemo#2](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_MDITabsDemo#2)]  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMDIFrameWndEx::EnableMDITabs](../vs140/CMDIFrameWndEx-Class.md#cmdiframewndex__enablemditabs)   
 [CMDITabInfo::m_bTabCustomTooltips](../vs140/CMDITabInfo-Class.md#cmditabinfo__m_btabcustomtooltips)