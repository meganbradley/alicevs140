---
title: "CTabView Class"
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
ms.assetid: 8e6ecd9d-d28d-432b-8ec8-0446f0204d52
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabView Class
The `CTabView` class simplifies the use of the tab control class ( [CMFCTabCtrl](../vs140/CTabView-Class.md)) in applications that use MFC's document/view architecture.  
  
## Syntax  
  
```  
class CTabbedView : public CView  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[AddView](#ctabview__addview)|Adds a new view to the tab control.|  
|[FindTab](#ctabview__findtab)|Returns the index of the specified view in the tab control.|  
|[GetActiveView](#ctabview__getactiveview)|Returns a pointer to the currently active view|  
|[GetTabControl](#ctabview__gettabcontrol)|Returns a reference to the tab control associated with the view.|  
|[RemoveView](#ctabview__removeview)|Removes the view from the tab control.|  
|[SetActiveView](#ctabview__setactiveview)|Makes a view active.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IsScrollBar](#ctabview__isscrollbar)|Called by the framework when creating a tab view to determine whether the tab view has a shared horizontal scroll bar.|  
|[OnActivateView](#ctabview__onactivateview)|Called by the framework when the tab view is made active or inactive.|  
  
## Remarks  
 This class makes it easy to put a tabbed view into a document/view application. `CTabView` is a `CView`-derived class that contains an embedded `CMFCTabCtrl` object. `CTabView` handles all messages required to support the `CMFCTabCtrl` object. Simply derive a class from `CTabView` and plug it into your application, then add `CView`-derived classes by using the `AddView` method. The tab control will display those views as tabs.  
  
 For example, you might have a document that can be represented in different ways: as a spreadsheet, a chart, an editable form, and so on. You can create individual views drawing the data as needed, insert them into your `CTabView`-derived object and have them tabbed without any additional coding.  
  
 [TabbedView Sample: MFC Tabbed View Application](../vs140/Visual-C---Samples.md) illustrates usage of `CTabView`.  
  
## Example  
 The following example shows how `CTabView` is used in the TabbedView sample.  
  
 [!CODE [NVC_MFC_TabbedView#1](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_TabbedView#1)]  
  
## Requirements  
 **Header:** afxTabView.h  
  
##  <a name="ctabview__addview"></a>  CTabView::AddView  
 Adds a view to the tab control.  
  
```  
int AddView(  
   CRuntimeClass* pViewClass,  
   const CString& strViewLabel,  
   int iIndex=-1,  
   CCreateContext* pContext=NULL   
);  
```  
  
### Parameters  
 [in] `pViewClass`  
 A pointer to a runtime class of the inserted view.  
  
 [in] `strViewLabel`  
 Specifies the tab's text.  
  
 [in] `iIndex`  
 Specifies the zero-based position at which to insert the view. If the position is -1 the new tab is inserted at the end.  
  
 [in] `pContext`  
 A pointer to the `CCreateContext` of the view.  
  
### Return Value  
 A view index if this method succeeds. Otherwise, -1.  
  
### Remarks  
 Call this function to add a view to the tab control that is embedded in a frame.  
  
##  <a name="ctabview__findtab"></a>  CTabView::FindTab  
 Returns the index of the specified view in the tab control.  
  
```  
int FindTab(  
   HWND hWndView   
) const;  
```  
  
### Parameters  
 [in] `hWndView`  
 The handle of the view.  
  
### Return Value  
 The index of the view if it is found; otherwise, -1.  
  
### Remarks  
 Call this function to retrieve the index of a view that has a specified handle.  
  
##  <a name="ctabview__getactiveview"></a>  CTabView::GetActiveView  
 Returns a pointer to the currently active view.  
  
```  
CView* GetActiveView() const;  
```  
  
### Return Value  
 A valid pointer to the active view, or `NULL` if there is no active view.  
  
### Remarks  
  
##  <a name="ctabview__gettabcontrol"></a>  CTabView::GetTabControl  
 Returns a reference to the tab control associated with the view.  
  
```  
DECLARE_DYNCREATE CMFCTabCtrl& GetTabControl();  
```  
  
### Return Value  
 A reference to the tab control associated with the view.  
  
##  <a name="ctabview__isscrollbar"></a>  CTabView::IsScrollBar  
 Called by the framework when creating a tab view to determine whether the tab view has a shared horizontal scroll bar.  
  
```  
virtual BOOL IsScrollBar() const;  
```  
  
### Return Value  
 `TRUE` if the tab view should be created together with a shared scroll bar. Otherwise, `FALSE`.  
  
### Remarks  
 The framework calls this method when a `CTabView` object is being created.  
  
 Override the `IsScrollBar` method in a `CTabView`-derived class and return `TRUE` if you want to create a view that has a shared horizontal scroll bar.  
  
##  <a name="ctabview__onactivateview"></a>  CTabView::OnActivateView  
 Called by the framework when the tab view is made active or inactive.  
  
```  
virtual void OnActivateView(  
   CView* view  
);  
```  
  
### Parameters  
 [in] `view`  
 A pointer to the view.  
  
### Remarks  
 The default implementation does nothing. Override this method in a `CTabView`-derived class to process this notification.  
  
##  <a name="ctabview__removeview"></a>  CTabView::RemoveView  
 Removes the view from the tab control.  
  
```  
BOOL RemoveView(  
   int iTabNum   
);  
```  
  
### Parameters  
 [in] `iTabNum`  
 The index of the view to remove.  
  
### Return Value  
 The index of the removed view if this method succeeds. Otherwise -1.  
  
### Remarks  
  
##  <a name="ctabview__setactiveview"></a>  CTabView::SetActiveView  
 Makes a view active.  
  
```  
BOOL SetActiveView(  
   int iTabNum   
);  
```  
  
### Parameters  
 [in] `iTabNum`  
 The zero-based index of the tab view.  
  
### Return Value  
 `TRUE` if the specified view was made active, `FALSE` if the view's index is invalid.  
  
### Remarks  
 For more information see [CMFCTabCtrl::SetActiveTab](../vs140/CMFCTabCtrl-Class.md#cmfctabctrl__setactivetab).  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCTabCtrl](../vs140/CTabView-Class.md)   
 [CView](../vs140/CView-Class.md)