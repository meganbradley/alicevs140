---
title: "CMFCPopupMenuBar Class"
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
ms.assetid: 4c93c459-7f70-4240-8c63-280bb811e374
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenuBar Class
A menu bar embedded into a pop-up menu.  
  
## Syntax  
  
```  
class CMFCPopupMenuBar : public CMFCToolBar  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCPopupMenuBar::AdjustSizeImmediate](#cmfcpopupmenubar__adjustsizeimmediate)|Immediately recalculates the layout of a pane. (Overrides [CPane::AdjustSizeImmediate](../vs140/CPane-Class.md#cpane__adjustsizeimmediate).)|  
|[CMFCPopupMenuBar::BuildOrigItems](#cmfcpopupmenubar__buildorigitems)|Loads popup menu items from a specified menu resource.|  
|[CMFCPopupMenuBar::CloseDelayedSubMenu](#cmfcpopupmenubar__closedelayedsubmenu)|Closes a delayed popup menu button.|  
|[CMFCPopupMenuBar::ExportToMenu](#cmfcpopupmenubar__exporttomenu)|Builds a menu from the popup-menu buttons.|  
|[CMFCPopupMenuBar::FindDestintationToolBar](#cmfcpopupmenubar__finddestintationtoolbar)|Locates the toolbar where a specified point lies.|  
|[CMFCPopupMenuBar::GetCurrentMenuImageSize](#cmfcpopupmenubar__getcurrentmenuimagesize)|Indicates the size of menu-button images.|  
|[CMFCPopupMenuBar::GetDefaultMenuId](#cmfcpopupmenubar__getdefaultmenuid)|Returns the identifier of the default menu item.|  
|[CMFCPopupMenuBar::GetLastCommandIndex](#cmfcpopupmenubar__getlastcommandindex)|Gets the index of the most recently invoked menu command.|  
|[CMFCPopupMenuBar::GetOffset](#cmfcpopupmenubar__getoffset)|Gets the row offset of the popup menu bar.|  
|[CMFCPopupMenuBar::ImportFromMenu](#cmfcpopupmenubar__importfrommenu)|Imports popup menu buttons from a specified menu.|  
|[CMFCPopupMenuBar::IsDropDownListMode](#cmfcpopupmenubar__isdropdownlistmode)|Indicates whether the popup menu bar is in drop-down-list mode.|  
|[CMFCPopupMenuBar::IsPaletteMode](#cmfcpopupmenubar__ispalettemode)|Indicates whether the popup menu bar is in palette mode.|  
|[CMFCPopupMenuBar::IsRibbonPanel](#cmfcpopupmenubar__isribbonpanel)|Indicates whether this is a ribbon panel ( `FALSE` by default).|  
|[CMFCPopupMenuBar::IsRibbonPanelInRegularMode](#cmfcpopupmenubar__isribbonpanelinregularmode)|Indicates whether this is a ribbon panel in regular mode ( `FALSE` by default).|  
|[CMFCPopupMenuBar::LoadFromHash](#cmfcpopupmenubar__loadfromhash)|Loads an archived menu.|  
|[CMFCPopupMenuBar::RestoreDelayedSubMenu](#cmfcpopupmenubar__restoredelayedsubmenu)|Restores a delayed menu button for closing the popup menu bar.|  
|[CMFCPopupMenuBar::SetButtonStyle](#cmfcpopupmenubar__setbuttonstyle)|Sets the style of the toolbar button at the given index. (Overrides [CMFCToolBar::SetButtonStyle](../Topic/CMFCToolBar%20Class.md#cmfctoolbar__setbuttonstyle).)|  
|[CMFCPopupMenuBar::SetOffset](#cmfcpopupmenubar__setoffset)|Sets the row offset of the popup menu bar.|  
|[CMFCPopupMenuBar::StartPopupMenuTimer](#cmfcpopupmenubar__startpopupmenutimer)|Starts the timer for a specified delayed popup menu button.|  
  
### Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCPopupMenuBar::m_bDisableSideBarInXPMode](#cmfcpopupmenubar__m_bdisablesidebarinxpmode)|Specifies whether the gray sidebar will be displayed when the application has a Windows XP appearance.|  
  
## Remarks  
 The `CMFCPopupMenuBar` is created at the same time as a [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md) and embedded inside it. The `CMFCPopupMenuBar` covers the entire client area of the `CMFCPopupMenu` object. It supports keyboard and mouse input. It also communicates that input to the `CMFCPopupMenu` and to the top-level frame window.  
  
## Example  
 The following example demonstrates how to initialize a `CMFCPopupMenuBar` object from a `CMFCPopupMenu` object. This code snippet is part of the [Draw Client sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_DrawClient#7](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_DrawClient#7)]  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CBasePane](../vs140/CBasePane-Class.md)  
  
 [CPane](../vs140/CPane-Class.md)  
  
 [CMFCBaseToolBar](../vs140/CMFCBaseToolBar-Class.md)  
  
 [CMFCToolBar](../Topic/CMFCToolBar%20Class.md)  
  
 [CMFCPopupMenuBar](../vs140/CMFCPopupMenuBar-Class.md)  
  
## Requirements  
 **Header:** afxpopupmenubar.h  
  
##  <a name="cmfcpopupmenubar__adjustsizeimmediate"></a>  CMFCPopupMenuBar::AdjustSizeImmediate  
 Immediately recalculates the layout of the popup menu bar pane. (Overrides [CPane::AdjustSizeImmediate](../vs140/CPane-Class.md#cpane__adjustsizeimmediate).  
  
```  
virtual void AdjustSizeImmediate(  
    BOOL bRecalcLayout  
);  
```  
  
### Parameters  
 [in] `bRecalcLayout`  
 `TRUE` to automatically recalculate the layout of the popup menu bar pane; otherwise, `FALSE`.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__buildorigitems"></a>  CMFCPopupMenuBar::BuildOrigItems  
 Loads popup menu items from a specified menu resource.  
  
```  
BOOL BuildOrigItems(  
   UINT uiMenuResID  
);  
```  
  
### Parameters  
 [in] `uiMenuResID`  
 Specifies the menu ID of the menu resource to load.  
  
### Return Value  
 Returns `TRUE` if successful or `FALSE` if not.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__closedelayedsubmenu"></a>  CMFCPopupMenuBar::CloseDelayedSubMenu  
 Closes a popup menu button that has been delayed.  
  
```  
virtual void CloseDelayedSubMenu();  
```  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__exporttomenu"></a>  CMFCPopupMenuBar::ExportToMenu  
 Builds a menu from the popup menu buttons.  
  
```  
virtual HMENU ExportToMenu() const;  
```  
  
### Return Value  
 Returns a handle to the new menu.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__finddestintationtoolbar"></a>  CMFCPopupMenuBar::FindDestintationToolBar  
 Locates the toolbar where a specified point lies.  
  
```  
CMFCToolBar* FindDestintationToolBar(  
   CPoint point  
);  
```  
  
### Parameters  
 [in] `point`  
 A point on the screen.  
  
### Return Value  
 Returns a handle to the toolbar where the point lies, if therei is one, or `NULL` if not.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__getcurrentmenuimagesize"></a>  CMFCPopupMenuBar::GetCurrentMenuImageSize  
 Indicates the size of menu-button images.  
  
```  
virtual CSize GetCurrentMenuImageSize( ) const;  
```  
  
### Return Value  
 Returns the size of menu-button images in the toolbar.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__getdefaultmenuid"></a>  CMFCPopupMenuBar::GetDefaultMenuId  
 Returns the identifier of the default menu item.  
  
```  
UINT GetDefaultMenuId( ) const;  
```  
  
### Return Value  
 Returns the identifier of the default menu item in the popup menu bar.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__getlastcommandindex"></a>  CMFCPopupMenuBar::GetLastCommandIndex  
 Gets the index of the most recently invoked menu command.  
  
```  
static int __stdcall GetLastCommandIndex( );  
```  
  
### Return Value  
 Returns the index of the last menu command that has been invoked.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__getoffset"></a>  CMFCPopupMenuBar::GetOffset  
 Gets the row offset of the popup menu bar.  
  
```  
int GetOffset() const;  
```  
  
### Return Value  
 Returns the row offset of the popup menu bar.  
  
### Remarks  
 This value is set using [CMFCPopupMenuBar::SetOffset](#cmfcpopupmenubar__setoffset).  
  
##  <a name="cmfcpopupmenubar__importfrommenu"></a>  CMFCPopupMenuBar::ImportFromMenu  
 Imports popup menu buttons from a specified menu.  
  
```  
virtual BOOL ImportFromMenu(  
   HMENU hMenu,  
   BOOL bShowAllCommands = FALSE  
);  
```  
  
### Parameters  
 [in] `hMenu`  
 The menu from which to import the popup menu buttons.  
  
 [in] `bShowAllCommands`  
 `TRUE` if all commands on the menu are to be imported, or `FALSE` if rarely used ones may be hidden.  
  
### Return Value  
 Returns `TRUE` if the menu buttons were successfully imported from the menu, or `FALSE` if not.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__isdropdownlistmode"></a>  CMFCPopupMenuBar::IsDropDownListMode  
 Indicates whether the popup menu bar is in drop-down-list mode.  
  
```  
BOOL IsDropDownListMode() const;  
```  
  
### Return Value  
 Returns `TRUE` if the popup menu bar is in drop-down-list mode, or `FALSE` if not.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__ispalettemode"></a>  CMFCPopupMenuBar::IsPaletteMode  
 Indicates whether the popup menu bar is in palette mode.  
  
```  
BOOL IsPaletteMode() const;  
```  
  
### Return Value  
 Returns `TRUE` if palette mode is enabled, or `FALSE` if not.  
  
### Remarks  
 When the menu bar is set to palette mode, menu items appear in multiple columns and a limited number of rows.  
  
##  <a name="cmfcpopupmenubar__isribbonpanel"></a>  CMFCPopupMenuBar::IsRibbonPanel  
 Indicates whether this is a ribbon panel ( `FALSE` by default).  
  
```  
virtual BOOL IsRibbonPanel() const;  
```  
  
### Return Value  
 Returns `FALSE` by default, indicating that this is not a ribbon panel.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__isribbonpanelinregularmode"></a>  CMFCPopupMenuBar::IsRibbonPanelInRegularMode  
 Indicates whether this is a ribbon panel in regular mode ( `FALSE` by default).  
  
```  
virtual BOOL IsRibbonPanelInRegularMode() const;  
```  
  
### Return Value  
 Returns `FALSE` by default, indicating that this is not a ribbon panel in regular mode.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__loadfromhash"></a>  CMFCPopupMenuBar::LoadFromHash  
 Loads an archived menu.  
  
```  
BOOL LoadFromHash(  
   HMENU hMenu  
);  
```  
  
### Parameters  
 [in] `hMenu`  
 A handle to the archived menu to load.  
  
### Return Value  
 Returns `TRUE` if the menu is loaded successfully, or `FALSE` if not.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__m_bdisablesidebarinxpmode"></a>  CMFCPopupMenuBar::m_bDisableSideBarInXPMode  
 A Boolean parameter that indicates whether your application has a gray sidebar when it has a Windows XP appearance.  
  
```  
BOOL m_bDisableSideBarInXPMode;  
```  
  
### Remarks  
 If this member variable is set to `FALSE` and your application has a Windows XP appearance, the framework draws a gray sidebar in your application.  
  
 The default value is `FALSE`.  
  
##  <a name="cmfcpopupmenubar__restoredelayedsubmenu"></a>  CMFCPopupMenuBar::RestoreDelayedSubMenu  
 Restores a delayed menu button for closing the popup menu bar.  
  
```  
virtual void RestoreDelayedSubMenu();  
```  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__setbuttonstyle"></a>  CMFCPopupMenuBar::SetButtonStyle  
 Sets the style of the toolbar button at the given index. (Overrides [CMFCToolBar::SetButtonStyle](../Topic/CMFCToolBar%20Class.md#cmfctoolbar__setbuttonstyle).)  
  
```  
virtual void SetButtonStyle(  
   int nIndex,  
   UINT nStyle  
);  
```  
  
### Parameters  
 [in] `nIndex`  
 The zero-based index of the toolbar button whose style is to be set.  
  
 [in] `nStyle`  
 The style of the button. See [ToolBar Control Styles](../vs140/ToolBar-Control-Styles.md) for the list of available toolbar button styles.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__setoffset"></a>  CMFCPopupMenuBar::SetOffset  
 Sets the row offset of the popup menu bar.  
  
```  
void SetOffset(  
   int iOffset  
);  
```  
  
### Parameters  
 [in] `iOffset`  
 The number of rows that the popup menu bar should be offset.  
  
### Remarks  
  
##  <a name="cmfcpopupmenubar__startpopupmenutimer"></a>  CMFCPopupMenuBar::StartPopupMenuTimer  
 Starts the timer for a specified delayed popup menu button.  
  
```  
void StartPopupMenuTimer(  
   CMFCToolBarMenuButton* pMenuButton,  
   int nDelayFactor = 1  
);  
```  
  
### Parameters  
 [in] `pMenuButton`  
 Pointer to the menu button for which to set the delay timer.  
  
 [in] `nDelayFactor`  
 A delay factor, equal to at least one, to multiply by the standard menu delay time (generally between a half second and five seconds).  
  
### Remarks  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)