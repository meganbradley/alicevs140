---
title: "CMFCVisualManagerWindows7 Class"
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
ms.assetid: e8d87df1-0c09-4b58-8ade-4e911f796e42
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerWindows7 Class
The `CMFCVisualManagerWindows7` gives an application the appearance of a [!INCLUDE[win7](../vs140/includes/win7_md.md)] application.  
  
## Syntax  
  
```  
class CMFCVisualManagerWindows7 : public CMFCVisualManagerWindows;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCVisualManagerWindows7::CMFCVisualManagerWindows7](#cmfcvisualmanagerwindows7__cmfcvisualmanagerwindows7)|Default constructor.|  
|[CMFCVisualManagerWindows7::~CMFCVisualManagerWindows7](#cmfcvisualmanagerwindows7__~cmfcvisualmanagerwindows7)|Default destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|`CMFCVisualManagerWindows7::CleanStyle`|Clears the current visual style and resets the default visual style.|  
|`CMFCVisualManagerWindows7::CleanUp`|Clears all of the objects in the user interface and resets the menus.|  
|`CMFCVisualManagerWindows7::DrawNcBtn`|Draws a button in the non-client area on the frame. The framework uses this method to draw minimize, maximize, close and restore buttons in the upper right corner of the window frame. This method is not called when the program uses a non-Aero theme.|  
|`CMFCVisualManagerWindows7::DrawNcText`|Draws text in the non-client area on the frame. The framework uses this method to draw the application title in the title bar at the top of the frame window.|  
|`CMFCVisualManagerWindows7::DrawSeparator`|Draws a separator on the [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md).|  
|`CMFCVisualManagerWindows7::GetRibbonBar`|Retrieves the [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md) associated with the user interface.|  
|[CMFCVisualManagerWindows7::GetRibbonEditBackgroundColor](#cmfcvisualmanagerwindows7__getribboneditbackgroundcolor)|Obtains a Ribbon edit box background color.|  
|`CMFCVisualManagerWindows7::GetRibbonPopupBorderSize`|Overrides [CMFCVisualManager::GetRibbonPopupBorderSize](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__getribbonpopupbordersize)|  
|`CMFCVisualManagerWindows7::GetRibbonQuickAccessToolBarChevronOffset`|Overrides [CMFCVisualManager::GetRibbonQuickAccessToolBarChevronOffset](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__getribbonquickaccesstoolbarchevronoffset)|  
|`CMFCVisualManagerWindows7::GetRibbonQuickAccessToolBarRightMargin`|Overrides [CMFCVisualManager::GetRibbonQuickAccessToolBarRightMargin](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__getribbonquickaccesstoolbarrightmargin)|  
|`CMFCVisualManagerWindows7::IsHighlightWholeMenuItem`|Overrides [CMFCVisualManagerWindows::IsHighlightWholeMenuItem](../vs140/CMFCVisualManagerWindows-Class.md#cmfcvisualmanagerwindows__ishighlightwholemenuitem)|  
|`CMFCVisualManagerWindows7::IsOwnerDrawMenuCheck`|Overrides [CMFCVisualManager::IsOwnerDrawMenuCheck](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__isownerdrawmenucheck)|  
|`CMFCVisualManagerWindows7::IsRibbonPresent`|Determines whether a `CMFCRibbonBar` is present and visible.|  
|`CMFCVisualManagerWindows7::OnDrawButtonBorder`|Overrides [CMFCVisualManagerWindows::OnDrawButtonBorder](../vs140/CMFCVisualManagerWindows-Class.md#cmfcvisualmanagerwindows__ondrawbuttonborder)|  
|`CMFCVisualManagerWindows7::OnDrawCheckBoxEx`|Overrides [CMFCVisualManagerWindows::OnDrawCheckBoxEx](../vs140/CMFCVisualManagerWindows-Class.md#cmfcvisualmanagerwindows__ondrawcheckboxex)|  
|`CMFCVisualManagerWindows7::OnDrawComboDropButton`|Overrides [CMFCVisualManagerWindows::OnDrawComboDropButton](../vs140/CMFCVisualManagerWindows-Class.md#cmfcvisualmanagerwindows__ondrawcombodropbutton)|  
|`CMFCVisualManagerWindows7::OnDrawDefaultRibbonImage`|Overrides [CMFCVisualManager::OnDrawDefaultRibbonImage](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawdefaultribbonimage)|  
|`CMFCVisualManagerWindows7::OnDrawMenuBorder`|Overrides [CMFCVisualManagerWindows::OnDrawMenuBorder](../vs140/CMFCVisualManagerWindows-Class.md#cmfcvisualmanagerwindows__ondrawmenuborder)|  
|`CMFCVisualManagerWindows7::OnDrawMenuCheck`|Overrides [CMFCVisualManager::OnDrawMenuCheck](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawmenucheck)|  
|`CMFCVisualManagerWindows7::OnDrawMenuLabel`|Overrides [CMFCVisualManager::OnDrawMenuLabel](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawmenulabel)|  
|`CMFCVisualManagerWindows7::OnDrawRadioButton`|Overrides `CMFCVisualManager::OnDrawRadioButton`|  
|`CMFCVisualManagerWindows7::OnDrawRibbonApplicationButton`|Overrides [CMFCVisualManager::OnDrawRibbonApplicationButton](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonapplicationbutton)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonButtonBorder`|Overrides [CMFCVisualManager::OnDrawRibbonButtonBorder](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonbuttonborder)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonCaption`|Overrides [CMFCVisualManager::OnDrawRibbonCaption](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribboncaption)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonCaptionButton`|Overrides [CMFCVisualManager::OnDrawRibbonCaptionButton](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribboncaptionbutton)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonCategory`|Overrides [CMFCVisualManager::OnDrawRibbonCategory](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribboncategory)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonCategoryTab`|Overrides [CMFCVisualManager::OnDrawRibbonCategoryTab](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribboncategorytab)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonDefaultPaneButton`|Overrides [CMFCVisualManager::OnDrawRibbonDefaultPaneButton](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbondefaultpanebutton)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonGalleryButton`|Overrides [CMFCVisualManager::OnDrawRibbonGalleryButton](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbongallerybutton)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonLaunchButton`|Overrides `CMFCVisualManager::OnDrawRibbonLaunchButton`|  
|`CMFCVisualManagerWindows7::OnDrawRibbonMenuCheckFrame`|Overrides [CMFCVisualManager::OnDrawRibbonMenuCheckFrame](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonmenucheckframe)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonPanel`|Overrides [CMFCVisualManager::OnDrawRibbonPanel](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonpanel)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonPanelCaption`|Overrides [CMFCVisualManager::OnDrawRibbonPanelCaption](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonpanelcaption)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonProgressBar`|Overrides [CMFCVisualManager::OnDrawRibbonProgressBar](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonprogressbar)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonRecentFilesFrame`|Overrides [CMFCVisualManager::OnDrawRibbonRecentFilesFrame](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonrecentfilesframe)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonSliderChannel`|Overrides [CMFCVisualManager::OnDrawRibbonSliderChannel](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonsliderchannel)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonSliderThumb`|Overrides [CMFCVisualManager::OnDrawRibbonSliderThumb](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonsliderthumb)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonSliderZoomButton`|Overrides [CMFCVisualManager::OnDrawRibbonSliderZoomButton](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonsliderzoombutton)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonStatusBarPane`|Overrides [CMFCVisualManager::OnDrawRibbonStatusBarPane](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbonstatusbarpane)|  
|`CMFCVisualManagerWindows7::OnDrawRibbonTabsFrame`|Overrides [CMFCVisualManager::OnDrawRibbonTabsFrame](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawribbontabsframe)|  
|`CMFCVisualManagerWindows7::OnDrawStatusBarSizeBox`|Overrides [CMFCVisualManagerWindows::OnDrawStatusBarSizeBox](../vs140/CMFCVisualManagerWindows-Class.md#cmfcvisualmanagerwindows__ondrawstatusbarsizebox)|  
|`CMFCVisualManagerWindows7::OnFillBarBackground`|Overrides [CMFCVisualManagerWindows::OnFillBarBackground](../vs140/CMFCVisualManagerWindows-Class.md#cmfcvisualmanagerwindows__onfillbarbackground)|  
|`CMFCVisualManagerWindows7::OnFillButtonInterior`|Overrides [CMFCVisualManagerWindows::OnFillButtonInterior](../vs140/CMFCVisualManagerWindows-Class.md#cmfcvisualmanagerwindows__onfillbuttoninterior)|  
|[CMFCVisualManagerWindows7::OnFillMenuImageRect](#cmfcvisualmanagerwindows7__onfillmenuimagerect)|The framework calls this method when it fills area around menu item images.|  
|`CMFCVisualManagerWindows7::OnFillRibbonButton`|Overrides [CMFCVisualManager::OnFillRibbonButton](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__onfillribbonbutton)|  
|`CMFCVisualManagerWindows7::OnFillRibbonQuickAccessToolBarPopup`|Overrides [CMFCVisualManager::OnFillRibbonQuickAccessToolBarPopup](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__onfillribbonquickaccesstoolbarpopup)|  
|`CMFCVisualManagerWindows7::OnHighlightMenuItem`|Overrides [CMFCVisualManagerWindows::OnHighlightMenuItem](../vs140/CMFCVisualManagerWindows-Class.md#cmfcvisualmanagerwindows__onhighlightmenuitem)|  
|`CMFCVisualManagerWindows7::OnNcActivate`|Overrides [CMFCVisualManager::OnNcActivate](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__onncactivate)|  
|`CMFCVisualManagerWindows7::OnNcPaint`|Overrides [CMFCVisualManager::OnNcPaint](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__onncpaint)|  
|`CMFCVisualManagerWindows7::OnUpdateSystemColors`|Overrides [CMFCVisualManagerWindows::OnUpdateSystemColors](../vs140/CMFCVisualManagerWindows-Class.md#cmfcvisualmanagerwindows__onupdatesystemcolors)|  
|`CMFCVisualManagerWindows7::SetResourceHandle`|Sets the resource handle that describes the attributes of the visual manager.|  
|`CMFCVisualManagerWindows7::SetStyle`|Sets the color scheme of the `CMFCVisualManagerWindows7` GUI.|  
  
## Remarks  
 Use the `CMFCVisualManagerWindows7` class to change the appearance of your application to mimic a default [!INCLUDE[win7](../vs140/includes/win7_md.md)] application. This class might not be valid if your application is running on a version of Windows earlier than [!INCLUDE[win7](../vs140/includes/win7_md.md)]. In that scenario, the application uses the default visual manager defined in [CMFCVisualManager](../vs140/CMFCVisualManager-Class.md).  
  
 The CMFCVisualManagerWindows7 inherits multiple methods from both the [CMFCVisualManagerWindows Class](../vs140/CMFCVisualManagerWindows-Class.md) and the `CMFCVisualManager` class. The methods listed in the previous section are methods new to the `CMFCVisualManagerWindows7` class.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CMFCBaseVisualManager](../vs140/CMFCBaseVisualManager-Class.md)  
  
 [CMFCVisualManager](../vs140/CMFCVisualManager-Class.md)  
  
 [CMFCVisualManagerOfficeXP](../vs140/CMFCVisualManagerOfficeXP-Class.md)  
  
 [CMFCVisualManagerWindows](../vs140/CMFCVisualManagerWindows-Class.md)  
  
 `CMFCVisualManagerWindows7`  
  
## Requirements  
 **Header:** afxvisualmanagerwindows7.h  
  
##  <a name="cmfcvisualmanagerwindows7___dtorcmfcvisualmanagerwindows7"></a>  CMFCVisualManagerWindows7::~CMFCVisualManagerWindows7  
 Default destructor.  
  
```  
virtual ~CMFCVisualManagerWindows7();  
```  
  
##  <a name="cmfcvisualmanagerwindows7__cmfcvisualmanagerwindows7"></a>  CMFCVisualManagerWindows7::CMFCVisualManagerWindows7  
 Default constructor.  
  
```  
CMFCVisualManagerWindows7();  
```  
  
##  <a name="cmfcvisualmanagerwindows7__getribboneditbackgroundcolor"></a>  CMFCVisualManagerWindows7::GetRibbonEditBackgroundColor  
 Obtains the background color of a ribbon edit box.  
  
```  
virtual COLORREF GetRibbonEditBackgroundColor (  
   CMFCRibbonRichEditCtrl* pEdit,  
   BOOL bIsHighlighted,  
   BOOL bIsPaneHighlighted,  
   BOOL bIsDisabled  
);  
```  
  
### Parameters  
 [in] `pEdit`  
 A pointer to the edit control. This value cannot be `NULL`.  
  
 [out] `bIsHighlighted`  
 Returns whether the ribbon box is highlighted.  
  
 [out] `bIsPaneHighlighted`  
 Returns `TRUE` if the ribbon panel that contains `pEdit` is highlighted.  
  
 [out] `bIsDisabled`  
 Returns whether `pEdit` is disabled.  
  
### Return Value  
 The background color of the edit box `pEdit`.  
  
### Remarks  
  
##  <a name="cmfcvisualmanagerwindows7__onfillmenuimagerect"></a>  CMFCVisualManagerWindows7::OnFillMenuImageRect  
 The framework calls this method when it fills area around a menu item image.  
  
```  
virtual void OnFillMenuImageRect(  
   CDC* pDC,  
   CMFCToolBarButton* pButton,  
   CRect rect,  
   CMFCVisualManager::AFX_BUTTON_STATE state  
);  
```  
  
### Parameters  
 [in] `pDC`  
 A pointer to the device context of a menu button.  
  
 [in] `pButton`  
 A pointer to a `CMFCToolBarButton`. The framework fills the background for this button.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the menu button image area.  
  
 [in] `state`  
 The button state.  
  
### Remarks  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [CMFCVisualManagerWindows Class](../vs140/CMFCVisualManagerWindows-Class.md)   
 [CMFCVisualManager::SetDefaultManager](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__setdefaultmanager)