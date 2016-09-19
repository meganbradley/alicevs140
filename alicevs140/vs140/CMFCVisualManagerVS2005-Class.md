---
title: "CMFCVisualManagerVS2005 Class"
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
ms.assetid: ea39b9ae-327e-4a51-bce7-dc84c78f005b
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerVS2005 Class
`CMFCVisualManagerVS2005` gives an application a Microsoft Visual Studio 2005 appearance.  
  
## Syntax  
  
```  
class CMFCVisualManagerVS2005 : public CMFCVisualManagerOffice2003  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCVisualManagerVS2005::GetDockingTabsBordersSize](#cmfcvisualmanagervs2005__getdockingtabsborderssize)|The framework calls this method when it draws a pane that is docked and tabbed. (Overrides [CMFCVisualManager::GetDockingTabsBordersSize](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__getdockingtabsborderssize).)|  
|[CMFCVisualManagerVS2005::GetMDITabsBordersSize](#cmfcvisualmanagervs2005__getmditabsborderssize)|The framework calls this method to determine the border size of a MDITabs window before it draws the window. (Overrides [CMFCVisualManager::GetMDITabsBordersSize](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__getmditabsborderssize).)|  
|[CMFCVisualManagerVS2005::GetPropertyGridGroupColor](#cmfcvisualmanagervs2005__getpropertygridgroupcolor)|(Overrides [CMFCVisualManagerOffice2003::GetPropertyGridGroupColor](../vs140/CMFCVisualManagerOffice2003-Class.md#cmfcvisualmanageroffice2003__getpropertygridgroupcolor).)|  
|[CMFCVisualManagerVS2005::GetTabFrameColors](#cmfcvisualmanagervs2005__gettabframecolors)|(Overrides [CMFCVisualManagerOffice2003::GetTabFrameColors](../vs140/CMFCVisualManagerOffice2003-Class.md#cmfcvisualmanageroffice2003__gettabframecolors).)|  
|[CMFCVisualManagerVS2005::HasOverlappedAutoHideButtons](#cmfcvisualmanagervs2005__hasoverlappedautohidebuttons)|Returns whether auto-hide buttons overlap in the current visual manager. (Overrides [CMFCVisualManager::HasOverlappedAutoHideButtons](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__hasoverlappedautohidebuttons).)|  
|[CMFCVisualManagerVS2005::OnDrawAutoHideButtonBorder](#cmfcvisualmanagervs2005__ondrawautohidebuttonborder)|(Overrides [CMFCVisualManagerOffice2003::OnDrawAutoHideButtonBorder](../vs140/CMFCVisualManagerOffice2003-Class.md#cmfcvisualmanageroffice2003__ondrawautohidebuttonborder).)|  
|[CMFCVisualManagerVS2005::OnDrawCaptionButton](#cmfcvisualmanagervs2005__ondrawcaptionbutton)|(Overrides `CMFCVisualManagerOfficeXP::OnDrawCaptionButton`.)|  
|[CMFCVisualManagerVS2005::OnDrawPaneCaption](#cmfcvisualmanagervs2005__ondrawpanecaption)|(Overrides [CMFCVisualManagerOffice2003::OnDrawPaneCaption](../vs140/CMFCVisualManagerOffice2003-Class.md#cmfcvisualmanageroffice2003__ondrawpanecaption).)|  
|[CMFCVisualManagerVS2005::OnDrawSeparator](#cmfcvisualmanagervs2005__ondrawseparator)|(Overrides [CMFCVisualManagerOffice2003::OnDrawSeparator](../vs140/CMFCVisualManagerOffice2003-Class.md#cmfcvisualmanageroffice2003__ondrawseparator).)|  
|[CMFCVisualManagerVS2005::OnDrawTab](#cmfcvisualmanagervs2005__ondrawtab)|(Overrides [CMFCVisualManagerOffice2003::OnDrawTab](../vs140/CMFCVisualManagerOffice2003-Class.md#cmfcvisualmanageroffice2003__ondrawtab).)|  
|[CMFCVisualManagerVS2005::OnDrawToolBoxFrame](#cmfcvisualmanagervs2005__ondrawtoolboxframe)|(Overrides [CMFCVisualManager::OnDrawToolBoxFrame](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawtoolboxframe).)|  
|[CMFCVisualManagerVS2005::OnEraseTabsArea](#cmfcvisualmanagervs2005__onerasetabsarea)|(Overrides [CMFCVisualManagerOffice2003::OnEraseTabsArea](../vs140/CMFCVisualManagerOffice2003-Class.md#cmfcvisualmanageroffice2003__onerasetabsarea).)|  
|[CMFCVisualManagerVS2005::OnFillAutoHideButtonBackground](#cmfcvisualmanagervs2005__onfillautohidebuttonbackground)|(Overrides [CMFCVisualManagerOffice2003::OnFillAutoHideButtonBackground](../vs140/CMFCVisualManagerOffice2003-Class.md#cmfcvisualmanageroffice2003__onfillautohidebuttonbackground).)|  
|[CMFCVisualManagerVS2005::OnFillHighlightedArea](#cmfcvisualmanagervs2005__onfillhighlightedarea)|(Overrides [CMFCVisualManagerOffice2003::OnFillHighlightedArea](../vs140/CMFCVisualManagerOffice2003-Class.md#cmfcvisualmanageroffice2003__onfillhighlightedarea).)|  
|[CMFCVisualManagerVS2005::OnFillMiniFrameCaption](#cmfcvisualmanagervs2005__onfillminiframecaption)|(Overrides `CMFCVisualManagerOfficeXP::OnFillMiniFrameCaption`.)|  
|[CMFCVisualManagerVS2005::OnUpdateSystemColors](#cmfcvisualmanagervs2005__onupdatesystemcolors)|(Overrides [CMFCVisualManagerOffice2003::OnUpdateSystemColors](../vs140/CMFCVisualManagerOffice2003-Class.md#cmfcvisualmanageroffice2003__onupdatesystemcolors).)|  
  
## Remarks  
 You use the CMFCVisualManagerVS2005 class to change the visual appearance of your application to resemble that of the [!INCLUDE[vsprvsext](../vs140/includes/vsprvsext_md.md)].  
  
 All of the members of this class are virtual functions that are derived from the ancestor of this class, [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md).  
  
## Example  
 The following example demonstrates how to use the visual manager VS 2005. This code snippet is part of the [Desktop Alert Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_DesktopAlertDemo#9](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_DesktopAlertDemo#9)]  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CMFCBaseVisualManager](../vs140/CMFCBaseVisualManager-Class.md)  
  
 [CMFCVisualManager](../vs140/CMFCVisualManager-Class.md)  
  
 [CMFCVisualManagerOfficeXP](../vs140/CMFCVisualManagerOfficeXP-Class.md)  
  
 [CMFCVisualManagerOffice2003](../vs140/CMFCVisualManagerOffice2003-Class.md)  
  
 [CMFCVisualManagerVS2005](../vs140/CMFCVisualManagerVS2005-Class.md)  
  
## Requirements  
 **Header:** afxvisualmanagervs2005.h  
  
##  <a name="cmfcvisualmanagervs2005__getdockingtabsborderssize"></a>  CMFCVisualManagerVS2005::GetDockingTabsBordersSize  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual int GetDockingTabsBordersSize();  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__getmditabsborderssize"></a>  CMFCVisualManagerVS2005::GetMDITabsBordersSize  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual int GetMDITabsBordersSize();  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__getpropertygridgroupcolor"></a>  CMFCVisualManagerVS2005::GetPropertyGridGroupColor  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual COLORREF GetPropertyGridGroupColor(  
   CMFCPropertyGridCtrl* pPropList  
);  
```  
  
### Parameters  
 [in] `pPropList`  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__gettabframecolors"></a>  CMFCVisualManagerVS2005::GetTabFrameColors  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void GetTabFrameColors(  
   const CMFCBaseTabCtrl* pTabWnd,  
   COLORREF& clrDark,  
   COLORREF& clrBlack,  
   COLORREF& clrHighlight,  
   COLORREF& clrFace,  
   COLORREF& clrDarkShadow,  
   COLORREF& clrLight,  
   CBrush*& pbrFace,  
   CBrush*& pbrBlack  
);  
```  
  
### Parameters  
 [in] `pTabWnd`  
  [in] `clrDark`  
  [in] `clrBlack`  
  [in] `clrHighlight`  
  [in] `clrFace`  
  [in] `clrDarkShadow`  
  [in] `clrLight`  
  [in] `pbrFace`  
  [in] `pbrBlack`  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__hasoverlappedautohidebuttons"></a>  CMFCVisualManagerVS2005::HasOverlappedAutoHideButtons  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual BOOL HasOverlappedAutoHideButtons() const;  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__ondrawautohidebuttonborder"></a>  CMFCVisualManagerVS2005::OnDrawAutoHideButtonBorder  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnDrawAutoHideButtonBorder(  
   CDC* pDC,  
   CRect rectBounds,  
   CRect rectBorderSize,  
   CMFCAutoHideButton* pButton  
);  
```  
  
### Parameters  
 [in] `pDC`  
  [in] `rectBounds`  
  [in] `rectBorderSize`  
  [in] `pButton`  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__ondrawcaptionbutton"></a>  CMFCVisualManagerVS2005::OnDrawCaptionButton  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnDrawCaptionButton(  
   CDC* pDC,  
   CMFCCaptionButton* pButton,  
   BOOL bActive,  
   BOOL bHorz,  
   BOOL bMaximized,  
   BOOL bDisabled,  
   int nImageID = -1  
);  
```  
  
### Parameters  
 [in] `pDC`  
  [in] `pButton`  
  [in] `bActive`  
  [in] `bHorz`  
  [in] `bMaximized`  
  [in] `bDisabled`  
  [in] `nImageID`  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__ondrawpanecaption"></a>  CMFCVisualManagerVS2005::OnDrawPaneCaption  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual COLORREF OnDrawPaneCaption(  
   CDC* pDC,  
   CDockablePane* pBar,  
   BOOL bActive,  
   CRect rectCaption,  
   CRect rectButtons  
);  
```  
  
### Parameters  
 [in] `pDC`  
  [in] `pBar`  
  [in] `bActive`  
  [in] `rectCaption`  
  [in] `rectButtons`  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__ondrawseparator"></a>  CMFCVisualManagerVS2005::OnDrawSeparator  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnDrawSeparator(  
   CDC* pDC,  
   CBasePane* pBar,  
   CRect rect,  
   BOOL bIsHoriz  
);  
```  
  
### Parameters  
 [in] `pDC`  
  [in] `pBar`  
  [in] `rect`  
  [in] `bIsHoriz`  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__ondrawtab"></a>  CMFCVisualManagerVS2005::OnDrawTab  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnDrawTab(  
   CDC* pDC,  
   CRect rectTab,  
   int iTab,  
   BOOL bIsActive,  
   const CMFCBaseTabCtrl* pTabWnd  
);  
```  
  
### Parameters  
 [in] `pDC`  
  [in] `rectTab`  
  [in] `iTab`  
  [in] `bIsActive`  
  [in] `pTabWnd`  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__ondrawtoolboxframe"></a>  CMFCVisualManagerVS2005::OnDrawToolBoxFrame  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnDrawToolBoxFrame(  
   CDC* pDC,  
   const CRect& rect  
);  
```  
  
### Parameters  
 [in] `pDC`  
  [in] `rect`  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__onerasetabsarea"></a>  CMFCVisualManagerVS2005::OnEraseTabsArea  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnEraseTabsArea(  
   CDC* pDC,  
   CRect rect,  
   const CMFCBaseTabCtrl* pTabWnd  
);  
```  
  
### Parameters  
 [in] `pDC`  
  [in] `rect`  
  [in] `pTabWnd`  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__onfillautohidebuttonbackground"></a>  CMFCVisualManagerVS2005::OnFillAutoHideButtonBackground  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnFillAutoHideButtonBackground(  
   CDC* pDC,  
   CRect rect,  
   CMFCAutoHideButton* pButton  
);  
```  
  
### Parameters  
 [in] `pDC`  
  [in] `rect`  
  [in] `pButton`  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__onfillhighlightedarea"></a>  CMFCVisualManagerVS2005::OnFillHighlightedArea  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnFillHighlightedArea(  
   CDC* pDC,  
   CRect rect,  
   CBrush* pBrush,  
   CMFCToolBarButton* pButton  
);  
```  
  
### Parameters  
 [in] `pDC`  
  [in] `rect`  
  [in] `pBrush`  
  [in] `pButton`  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__onfillminiframecaption"></a>  CMFCVisualManagerVS2005::OnFillMiniFrameCaption  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual COLORREF OnFillMiniFrameCaption(  
   CDC* pDC,  
   CRect rectCaption,  
   CPaneFrameWnd* pFrameWnd,  
   BOOL bActive  
);  
```  
  
### Parameters  
 [in] `pDC`  
  [in] `rectCaption`  
  [in] `pFrameWnd`  
  [in] `bActive`  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcvisualmanagervs2005__onupdatesystemcolors"></a>  CMFCVisualManagerVS2005::OnUpdateSystemColors  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnUpdateSystemColors();  
```  
  
### Remarks  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [CMFCVisualManagerOfficeXP Class](../vs140/CMFCVisualManagerOfficeXP-Class.md)   
 [CMFCVisualManagerWindows Class](../vs140/CMFCVisualManagerWindows-Class.md)   
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [CMFCVisualManager::SetDefaultManager](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__setdefaultmanager)