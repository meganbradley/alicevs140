---
title: "CTooltipManager Class"
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
ms.assetid: c71779d7-8b6e-47ef-8500-d4552731fe86
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTooltipManager Class
Maintains runtime information about tooltips. The `CTooltipManager` class is instantiated one time per application.  
  
## Syntax  
  
```  
class CTooltipManager : public CObject  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CTooltipManager::CreateToolTip](#ctooltipmanager__createtooltip)|Creates a tooltip control for the specified Windows control type(s).|  
|[CTooltipManager::DeleteToolTip](#ctooltipmanager__deletetooltip)|Deletes a tooltip control.|  
|[CTooltipManager::SetTooltipParams](#ctooltipmanager__settooltipparams)|Customizes the visual appearance of the tooltip control for the specified Windows control type(s).|  
|[CTooltipManager::SetTooltipText](#ctooltipmanager__settooltiptext)|Sets the text and description for a tooltip control.|  
|[CTooltipManager::UpdateTooltips](#ctooltipmanager__updatetooltips)||  
  
## Remarks  
 Use [CMFCToolTipCtrl](../vs140/CMFCToolTipCtrl-Class.md), `CMFCToolTipInfo`, and `CTooltipManager` together to implement customized tooltips in your application. For an example of how to use these tooltip classes, see the [CMFCToolTipCtrl](../vs140/CMFCToolTipCtrl-Class.md) topic.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CTooltipManager](../vs140/CTooltipManager-Class.md)  
  
## Requirements  
 **Header:** afxtooltipmanager.h  
  
##  <a name="ctooltipmanager__createtooltip"></a>  CTooltipManager::CreateToolTip  
 Creates a tooltip control.  
  
```  
static BOOL CreateToolTip(  
   CToolTipCtrl*& pToolTip,  
   CWnd* pWndParent,  
   UINT nType   
);  
```  
  
### Parameters  
 [out]  `pToolTip`  
 A reference to a tooltip pointer. It is set to point to the newly created tooltip when the function returns.  
  
 [in]  `pWndParent`  
 Parent of the tooltip.  
  
 [in]  `nType`  
 Type of the tooltip.  
  
### Return Value  
 Nonzero if a tooltip has been created successfully.  
  
### Remarks  
 You must call [CTooltipManager::DeleteTooltip](#ctooltipmanager__deletetooltip) to delete the tooltip control that is passed back in `pToolTip`.  
  
 The [CTooltipManager](../vs140/CTooltipManager-Class.md) sets the visual display parameters of each tooltip it creates based on the tooltip type that `nType` specifies. To change the parameters for one or more tooltip types, call [CTooltipManager::SetTooltipParams](#ctooltipmanager__settooltipparams).  
  
 Valid tooltip types are listed in the following table:  
  
|Tooltip type|Control category|Example types|  
|------------------|----------------------|-------------------|  
|AFX_TOOLTIP_TYPE_BUTTON|A button.|CMFCButton|  
|AFX_TOOLTIP_TYPE_CAPTIONBAR|A caption bar.|CMFCCaptionBar|  
|AFX_TOOLTIP_TYPE_DEFAULT|Any control that does not fit another category.|None.|  
|AFX_TOOLTIP_TYPE_DOCKBAR|A dockable pane.|CDockablePane|  
|AFX_TOOLTIP_TYPE_EDIT|A text box.|None.|  
|AFX_TOOLTIP_TYPE_MINIFRAME|A miniframe.|CPaneFrameWnd|  
|AFX_TOOLTIP_TYPE_PLANNER|A planner.|None.|  
|AFX_TOOLTIP_TYPE_RIBBON|A ribbon bar.|CMFCRibbonBar, CMFCRibbonPanelMenuBar|  
|AFX_TOOLTIP_TYPE_TAB|A tab control.|CMFCTabCtrl|  
|AFX_TOOLTIP_TYPE_TOOLBAR|A toolbar.|CMFCToolBar, CMFCPopupMenuBar|  
|AFX_TOOLTIP_TYPE_TOOLBOX|A toolbox.|None.|  
  
##  <a name="ctooltipmanager__deletetooltip"></a>  CTooltipManager::DeleteToolTip  
 Deletes a tooltip control.  
  
```  
static void DeleteToolTip(  
   CToolTipCtrl*& pToolTip   
);  
```  
  
### Parameters  
 [in, out]  `pToolTip`  
 A reference to a pointer to a tooltip to be destroyed.  
  
### Remarks  
 Call this method for each [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) that was created by [CTooltipManager::CreateToolTip](#ctooltipmanager__createtooltip). The parent control should call this method from its `OnDestroy` handler. This is required to correctly remove the tooltip from the framework. This method sets `pToolTip` to `NULL` before it returns.  
  
##  <a name="ctooltipmanager__settooltipparams"></a>  CTooltipManager::SetTooltipParams  
 Customizes the appearance of the tooltip control for the specified Windows control types.  
  
```  
void SetTooltipParams(  
   UINT nTypes,  
   CRuntimeClass* pRTC=RUNTIME_CLASS( CMFCToolTipCtrl),  
   CMFCToolTipInfo* pParams=NULL   
);  
```  
  
### Parameters  
 [in]  `nTypes`  
 Specifies control types.  
  
 [in]  `pRTC`  
 Runtime class of custom tooltip.  
  
 [in]  `pParams`  
 Tooltip parameters.  
  
### Remarks  
 This method sets the runtime class and initial parameters that the [CToolTipManager](../vs140/CTooltipManager-Class.md) uses when it creates tooltips. When a control calls [CMFCTooltipManager::CreateToolTip](#ctooltipmanager__createtooltip) and passes in a tooltip type that is one of the types indicated by `nTypes`, the tooltip manager creates a tooltip control that is an instance of the runtime class specified by `pRTC` and passes the parameters specified by `pParams` to the new tooltip.  
  
 When you call this method, all existing tooltip owners receive the AFX_WM_UPDATETOOLTIPS message and they must re-create their tooltips by using [CMFCTooltipManager::CreateToolTip](#ctooltipmanager__createtooltip).  
  
 `nTypes` can be any combination of the valid tooltip types that [CreateToolTip](#ctooltipmanager__createtooltip) uses, or it can be AFX_TOOLTIP_TYPE_ALL. If you pass AFX_TOOLTIP_TYPE_ALL, all tooltip types are affected.  
  
### Example  
 The following example demonstrates how to use the `SetTooltipParams` method of the `CTooltipManager` class. This code snippet is part of the [Draw Client sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_DrawClient#11](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_DrawClient#11)]  
  
##  <a name="ctooltipmanager__settooltiptext"></a>  CTooltipManager::SetTooltipText  
 Sets the text and description for a tooltip.  
  
```  
static void SetTooltipText(  
   TOOLINFO* pTI,  
   CToolTipCtrl* pToolTip,  
   UINT nType,  
   const CString strText,  
   LPCTSTR lpszDescr=NULL   
);  
```  
  
### Parameters  
 [in]  `pTI`  
 A pointer to a TOOLINFO object.  
  
 [in, out]  `pToolTip`  
 A pointer to the tooltip control for which to set the text and description.  
  
 [in]  `nType`  
 Specifies the type of control with which this tooltip is associated.  
  
 [in]  `strText`  
 The text to set as the tooltip text.  
  
 [in]  `lpszDescr`  
 A pointer to the tooltip description. Can be `NULL`.  
  
### Remarks  
 The value of `nType` must be the same value as the `nType` parameter of [CMFCTooltipManager::CreateToolTip](#ctooltipmanager__createtooltip) when you created the tooltip.  
  
##  <a name="ctooltipmanager__updatetooltips"></a>  CTooltipManager::UpdateTooltips  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void UpdateTooltips();  
```  
  
### Remarks  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCToolTipCtrl](../vs140/CMFCToolTipCtrl-Class.md)   
 [CMFCToolTipInfo](../vs140/CMFCToolTipInfo-Class.md)