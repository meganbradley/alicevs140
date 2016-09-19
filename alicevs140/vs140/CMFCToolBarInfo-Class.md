---
title: "CMFCToolBarInfo Class"
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
ms.assetid: 6dc84482-eaaa-491f-aa5d-dd7a57886b46
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarInfo Class
Contains the resource IDs of toolbar images in various states. `CMFCToolBarInfo` is a helper class that is used as a parameter of the [CMFCToolBar::LoadToobarEx](../Topic/CMFCToolBar%20Class.md#cmfctoolbar__loadtoolbarex) method.  
  
## Syntax  
  
```  
class CMFCToolBarInfo  
```  
  
## Members  
  
### Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCToolBarInfo::m_uiColdResID](#cmfctoolbarinfo__m_uicoldresid)|Resource ID of the toolbar bitmap that contains regular (cold) toolbar images.|  
|[CMFCToolBarInfo::m_uiDisabledResID](#cmfctoolbarinfo__m_uidisabledresid)|Resource ID of the toolbar bitmap that contains disabled toolbar images.|  
|[CMFCToolBarInfo::m_uiHotResID](#cmfctoolbarinfo__m_uihotresid)|Resource ID of the toolbar bitmap that contains selected (hot) toolbar images.|  
|[CMFCToolBarInfo::m_uiLargeColdResID](#cmfctoolbarinfo__m_uilargecoldresid)|Resource ID of the toolbar bitmap that contains large, regular toolbar images.|  
|[CMFCToolBarInfo::m_uiLargeDisabledResID](#cmfctoolbarinfo__m_uilargedisabledresid)|Resource ID of the toolbar bitmap that contains large, disabled toolbar images.|  
|[CMFCToolBarInfo::m_uiLargeHotResID](#cmfctoolbarinfo__m_uilargehotresid)|Resource ID of the toolbar bitmap that contains large, selected toolbar images.|  
|[CMFCToolBarInfo::m_uiMenuDisabledResID;](#cmfctoolbarinfo__m_uimenudisabledresid)|Resource ID of the toolbar bitmap that contains disabled menu images.|  
|[CMFCToolBarInfo::m_uiMenuResID](#cmfctoolbarinfo__m_uimenuresid)|Resource ID of the toolbar bitmap that contains menu images.|  
  
## Remarks  
 A full toolbar bitmap consists of small toolbar images (buttons) of a fixed size. Each resource ID that is stored in a `CMFCToolBarInfo` object is a bitmap that contains a full set of toolbar images in a single state (for example, selected, disabled, large, or menu images).  
  
## Inheritance Hierarchy  
 [CMFCToolBarInfo](../vs140/CMFCToolBarInfo-Class.md)  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
##  <a name="cmfctoolbarinfo__m_uicoldresid"></a>  CMFCToolBarInfo::m_uiColdResID  
 Specifies a resource ID for all the regular button images of a toolbar.  
  
```  
UINT m_uiColdResID;  
```  
  
##  <a name="cmfctoolbarinfo__m_uidisabledresid"></a>  CMFCToolBarInfo::m_uiDisabledResID  
 Specifies a resource ID for the button-unavailable images of a toolbar.  
  
```  
UINT m_uiDisabledResID;  
```  
  
##  <a name="cmfctoolbarinfo__m_uihotresid"></a>  CMFCToolBarInfo::m_uiHotResID  
 Specifies a resource ID for all the highlighted button images of a toolbar.  
  
```  
UINT m_uiHotResID  
```  
  
##  <a name="cmfctoolbarinfo__m_uilargecoldresid"></a>  CMFCToolBarInfo::m_uiLargeColdResID  
 Specifies a resource ID for all the large regular button images of a toolbar.  
  
```  
UINT m_uiLargeColdResID  
```  
  
##  <a name="cmfctoolbarinfo__m_uilargedisabledresid"></a>  CMFCToolBarInfo::m_uiLargeDisabledResID  
 Specifies a resource ID for all the large disabled button images of a toolbar.  
  
```  
UINT m_uiLargeDisabledResID;  
```  
  
##  <a name="cmfctoolbarinfo__m_uilargehotresid"></a>  CMFCToolBarInfo::m_uiLargeHotResID  
 Specifies a resource ID for all the large highlighted images of a toolbar.  
  
```  
UINT m_uiLargeHotResID;  
```  
  
##  <a name="cmfctoolbarinfo__m_uimenudisabledresid"></a>  CMFCToolBarInfo::m_uiMenuDisabledResID  
 Specifies a resource ID for the command-unavailable images of a toolbar.  
  
```  
UINT m_uiMenuDisabledResID;  
```  
  
##  <a name="cmfctoolbarinfo__m_uimenuresid"></a>  CMFCToolBarInfo::m_uiMenuResID  
 Specifies a resource ID for all the regular menu item images of a toolbar.  
  
```  
UINT m_uiMenuResID;  
```  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCToolBar](../Topic/CMFCToolBar%20Class.md)   
 [CMFCToolBar::LoadToobarEx](../Topic/CMFCToolBar%20Class.md#cmfctoolbar__loadtoolbarex)