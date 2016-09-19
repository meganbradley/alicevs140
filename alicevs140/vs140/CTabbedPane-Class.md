---
title: "CTabbedPane Class"
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
ms.assetid: f4dc5215-b789-4f2d-8c62-477aceda3578
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabbedPane Class
Implements the functionality of a pane with detachable tabs.  
  
## Syntax  
  
```  
class CTabbedPane : public CBaseTabbedPane  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|`CTabbedPane::CTabbedPane`|Default constructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CTabbedPane::DetachPane](#ctabbedpane__detachpane)|(Overrides [CBaseTabbedPane::DetachPane](../vs140/CBaseTabbedPane-Class.md#cbasetabbedpane__detachpane).)|  
|[CTabbedPane::EnableTabAutoColor](#ctabbedpane__enabletabautocolor)|Enables or disables automatic coloring of tabs.|  
|[CTabbedPane::FloatTab](#ctabbedpane__floattab)|Floats a pane, but only if the pane currently resides in a detachable tab. (Overrides [CBaseTabbedPane::FloatTab](../vs140/CBaseTabbedPane-Class.md#cbasetabbedpane__floattab).)|  
|[CTabbedPane::GetTabArea](#ctabbedpane__gettabarea)|Returns the size and position of the tab area within the tabbed window.|  
|[CTabbedPane::GetTabWnd](#ctabbedpane__gettabwnd)||  
|[CTabbedPane::HasAutoHideMode](#ctabbedpane__hasautohidemode)|Determines whether the tabbed pane can be switched to autohide mode. (Overrides [CBaseTabbedPane::HasAutoHideMode](../vs140/CBaseTabbedPane-Class.md#cbasetabbedpane__hasautohidemode).)|  
|[CTabbedPane::IsTabLocationBottom](#ctabbedpane__istablocationbottom)|Determines whether the tabs are located at the bottom of the window.|  
|[CTabbedPane::ResetTabs](#ctabbedpane__resettabs)|Resets all tabbed panes to the default state.|  
|[CTabbedPane::SetTabAutoColors](#ctabbedpane__settabautocolors)|Sets a list of custom colors that can be used when the auto color feature is enabled.|  
  
### Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CTabbedPane::m_bTabsAlwaysTop](#ctabbedpane__m_btabsalwaystop)|The default location for tabs in the application.|  
|[CTabbedPane::m_pTabWndRTC](#ctabbedpane__m_ptabwndrtc)|Runtime class information for a custom `CMFCTabCtrl`-derived object.|  
  
## Remarks  
 The framework automatically creates an instance of this class when a user attaches one pane to another by pointing to the caption of the second pane. All of the tabbed panes that are created by the framework have an ID of -1.  
  
 To specify regular tabs instead of Outlook-style tabs, pass the `AFX_CBRS_REGULAR_TABS` style to the [CDockablePane::CreateEx](../vs140/CDockablePane-Class.md#cdockablepane__createex) method.  
  
 If you create a tabbed pane with detachable tabs, the pane may be destroyed automatically by the framework, so you should not store the pointer. To get a pointer to the tabbed pane, call the `CBasePane::GetParentTabbedPane` method.  
  
## Example  
 In this example we create a `CTabbedPane` object. Next, we use [CBaseTabbedPane::AddTab](../vs140/CBaseTabbedPane-Class.md#cbasetabbedpane__addtab) to attach additional tabs.  
  
```  
CTabbedPane* pTabbededBar = new CTabbedPane (TRUE);  
if (!pTabbededBar->Create (_T(""), this, CRect (0, 0, 200, 200),  
                           TRUE,   
                           (UINT) -1,  
                           WS_CHILD | WS_VISIBLE | WS_CLIPSIBLINGS |  
                           WS_CLIPCHILDREN | CBRS_LEFT |    
                           CBRS_FLOAT_MULTI))  
{  
    TRACE0("Failed to create Solution Explorer bar\n");  
    return FALSE;      // fail to create  
}  
  
pTabbededBar->AddTab (&m_wndClassView);  
pTabbededBar->AddTab (&m_wndResourceView);  
pTabbededBar->AddTab (&m_wndFileView);  
pTabbededBar->EnableDocking(CBRS_ALIGN_ANY);  
DockPane(pTabbededBar);  
```  
  
## Example  
 Another way to create a tabbed control bar object is to use [CDockablePane::AttachToTabWnd](../vs140/CDockablePane-Class.md#cdockablepane__attachtotabwnd). The `AttachToTabWnd` method dynamically creates a tabbed pane object using runtime class information set by [CDockablePane::SetTabbedPaneRTC](../vs140/CDockablePane-Class.md#cdockablepane__settabbedpanertc).  
  
 In this example we create a tabbed pane dynamically, attach two tabs, and make the second tab non-detachable.  
  
```  
DockPane(&m_wndClassView);  
CTabbedPane* pTabbedBar = NULL;  
m_wndResourceView.AttachToTabWnd (&m_wndClassView, DM_SHOW, TRUE,  
                                  (CDockablePane**) &pTabbedBar);  
m_wndFileView.AttachToTabWnd (pTabbedBar, DM_SHOW, TRUE,  
                              (CDockablePane**) &pTabbedBar);  
pTabbedBar->GetUnderlyingWindow ()->EnableTabDetach (1, FALSE);  
```  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CBasePane](../vs140/CBasePane-Class.md)  
  
 [CPane](../vs140/CPane-Class.md)  
  
 [CDockablePane](../vs140/CDockablePane-Class.md)  
  
 [CBaseTabbedPane](../vs140/CBaseTabbedPane-Class.md)  
  
 [CTabbedPane](../vs140/CTabbedPane-Class.md)  
  
## Requirements  
 **Header:** afxTabbedPane.h  
  
##  <a name="ctabbedpane__detachpane"></a>  CTabbedPane::DetachPane  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual BOOL DetachPane(  
   CWnd* pBar,  
   BOOL bHide = FALSE  
);  
```  
  
### Parameters  
 [in] `pBar`  
  [in] `bHide`  
  
### Return Value  
  
### Remarks  
  
##  <a name="ctabbedpane__enabletabautocolor"></a>  CTabbedPane::EnableTabAutoColor  
 Enables or disables automatic coloring of tabs.  
  
```  
static void EnableTabAutoColor(  
    BOOL bEnable = TRUE  
);  
```  
  
### Parameters  
 [in] `bEnable`  
 `TRUE` to enable auto coloring of tabs; otherwise, `FALSE`.  
  
### Remarks  
 Use this static method to enable or disable automatic coloring of tabs in all tabbed panes in the application. When this feature is enabled, each tab is filled by its own color. You can find the list of colors that are used to color the tabs by calling the [CMFCBaseTabCtrl::GetAutoColors](../vs140/CMFCBaseTabCtrl-Class.md#cmfcbasetabctrl__getautocolors) method.  
  
 You can specify the list of colors that will be used for tabs by calling [CTabbedPane::SetTabAutoColors](#ctabbedpane__settabautocolors).  
  
 By default, this option is disabled.  
  
##  <a name="ctabbedpane__floattab"></a>  CTabbedPane::FloatTab  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual BOOL FloatTab(  
   CWnd* pBar,  
   int nTabID,  
   AFX_DOCK_METHOD dockMethod,  
   BOOL bHide = FALSE  
);  
```  
  
### Parameters  
 [in] `pBar`  
  [in] `nTabID`  
  [in] `dockMethod`  
  [in] `bHide`  
  
### Return Value  
  
### Remarks  
  
##  <a name="ctabbedpane__gettabarea"></a>  CTabbedPane::GetTabArea  
 Returns the size and position of the tab area in the tabbed window.  
  
```  
virtual void GetTabArea(  
    CRect& rectTabAreaTop,  
    CRect& rectTabAreaBottom   
) const;  
```  
  
### Parameters  
 [out] `rectTabAreaTop`  
 Contains the size and position, in screen coordinates, of the top tab area.  
  
 [out] `rectTabAreaBottom`  
 Contains the size and position, in screen coordinates, of the bottom tab area.  
  
### Remarks  
 The framework calls this method to determine how to dock a pane that a user is dragging. When the user drags a pane over the tab area of the target pane, the framework tries to add it as a new tab of the target pane. Otherwise, it tries to dock the pane to the side of the target pane, which involves creating a new pane container with a pane divider that separates the two panes.  
  
 Override this method in a `CTabbedPane`-derived class to change this behavior.  
  
##  <a name="ctabbedpane__gettabwnd"></a>  CTabbedPane::GetTabWnd  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
CMFCTabCtrl* GetTabWnd() const;  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="ctabbedpane__hasautohidemode"></a>  CTabbedPane::HasAutoHideMode  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual BOOL HasAutoHideMode() const;  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="ctabbedpane__istablocationbottom"></a>  CTabbedPane::IsTabLocationBottom  
 Determines whether the tabs are located at the bottom of the window.  
  
```  
virtual BOOL IsTabLocationBottom() const;  
```  
  
### Return Value  
 `TRUE` if the tab area is located at the bottom of the tabbed window; otherwise, `FALSE`.  
  
### Remarks  
  
##  <a name="ctabbedpane__m_btabsalwaystop"></a>  CTabbedPane::m_bTabsAlwaysTop  
 The default location for tabs in the application.  
  
```  
AFX_IMPORT_DATA static BOOL m_bTabsAlwaysTop;  
```  
  
### Remarks  
 Set this static member to `TRUE` to force all tabs in the application to be displayed at the top of the tabbed pane.  
  
 You must set this value before a tabbed pane has been created.  
  
 The default value is `FALSE`.  
  
##  <a name="ctabbedpane__m_ptabwndrtc"></a>  CTabbedPane::m_pTabWndRTC  
 Runtime class information for a custom `CMFCTabCtrl`-derived object.  
  
```  
AFX_IMPORT_DATA static CRuntimeClass* m_pTabWndRTC;  
```  
  
### Remarks  
 Set this static member variable to a pointer to the runtime class information of a `CMFCTabCtrl`-derived object if you are using a custom tabbed window inside a tabbed pane.  
  
##  <a name="ctabbedpane__resettabs"></a>  CTabbedPane::ResetTabs  
 Resets all tabbed panes to the default state.  
  
```  
static void ResetTabs();  
```  
  
### Remarks  
 Call this method to revert all tabbed panes to their default state. When called, this method resets the border sizes and auto color state of all tabbed panes.  
  
##  <a name="ctabbedpane__settabautocolors"></a>  CTabbedPane::SetTabAutoColors  
 Sets a list of custom colors that are used when the auto color feature is enabled.  
  
```  
static void SetTabAutoColors(  
    const CArray<COLORREF, COLORREF>& arColors  
);  
```  
  
### Parameters  
 [in] `arColors`  
 Contains the array of colors to set.  
  
### Remarks  
 Use this method to customize the list of colors that are used when the auto color feature is enabled. This is a static function and affects all tabbed panes in your application.  
  
 Use [CTabbedPane::EnableTabAutoColor](#ctabbedpane__enabletabautocolor) to enable or disable the auto color feature.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)   
 [CMFCOutlookBar](../vs140/CMFCOutlookBar-Class.md)