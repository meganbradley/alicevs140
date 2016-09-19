---
title: "CMFCMenuButton Class"
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
ms.assetid: 53d3d459-1e5a-47c5-8b7f-2e61f6af5187
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuButton Class
A button that displays a pop-up menu and reports on the user's menu selections.  
  
## Syntax  
  
```  
class CMFCMenuButton : public CMFCButton  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCMenuButton::CMFCMenuButton](#cmfcmenubutton__cmfcmenubutton)|Constructs a `CMFCMenuButton` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCMenuButton::PreTranslateMessage](#cmfcmenubutton__pretranslatemessage)|Called by the framework to translate window messages before they are dispatched. (Overrides `CMFCButton::PreTranslateMessage`.)|  
|[CMFCMenuButton::SizeToContent](#cmfcmenubutton__sizetocontent)|Changes the size of the button according to its text and image size.|  
  
### Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCMenuButton::m_bOSMenu](#cmfcmenubutton__m_bosmenu)|Specifies whether to display the default system pop-up menu or to use [CContextMenuManager::TrackPopupMenu](../vs140/CContextMenuManager-Class.md#ccontextmenumanager__trackpopupmenu).|  
|[CMFCMenuButton::m_bRightArrow](#cmfcmenubutton__m_brightarrow)|Specifies whether the pop-up menu will appear underneath or to the right of the button.|  
|[CMFCMenuButton::m_bStayPressed](#cmfcmenubutton__m_bstaypressed)|Specifies whether the menu button changes its state after the user releases the button.|  
|[CMFCMenuButton::m_hMenu](#cmfcmenubutton__m_hmenu)|A handle to the attached Windows menu.|  
|[CMFCMenuButton::m_nMenuResult](#cmfcmenubutton__m_nmenuresult)|An identifier that indicates which item the user selected from the pop-up menu.|  
  
## Remarks  
 The `CMFCMenuButton` class is derived from the [CMFCButton Class](../vs140/CMFCButton-Class.md) which is, in turn, derived from the [CButton Class](../vs140/CButton-Class.md). Therefore, you can use `CMFCMenuButton` in your code the same way you would use `CButton`.  
  
 When you create a `CMFCMenuButton`, you must pass in a handle to the associated pop-up menu. Next, call the function `CMFCMenuButton::SizeToContent`. `CMFCMenuButton::SizeToContent` checks that the button size is sufficient to include an arrow that points to the location where the pop-up window will appear - namely, underneath or to the right of the button.  
  
## Example  
 The following example demonstrates how to set the handle of the menu attached to the button, resize the button according to its text and image size, and set the pop-up menu that is displayed by the framework. This code snippet is part of the [New Controls sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_NewControls#38](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#38)]  
[!CODE [NVC_MFC_NewControls#39](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#39)]  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CButton](../vs140/CButton-Class.md)  
  
 [CMFCButton](../vs140/CMFCButton-Class.md)  
  
 [CMFCMenuButton](../vs140/CMFCMenuButton-Class.md)  
  
## Requirements  
 **Header:** afxmenubutton.h  
  
##  <a name="cmfcmenubutton__cmfcmenubutton"></a>  CMFCMenuButton::CMFCMenuButton  
 Constructs a new [CMFCMenuButton](../vs140/CMFCMenuButton-Class.md) object.  
  
```  
CMFCMenuButton();  
```  
  
##  <a name="cmfcmenubutton__m_bosmenu"></a>  CMFCMenuButton::m_bOSMenu  
 A Boolean member variable that indicates which pop-up menu the framework displays.  
  
```  
BOOL m_bOSMenu;  
```  
  
### Remarks  
 If `m_bOSMenu` is `TRUE`, the framework calls the inherited `TrackPopupMenu` method for this object. Otherwise, the framework calls [CContextMenuManager::TrackPopupMenu](../vs140/CContextMenuManager-Class.md#ccontextmenumanager__trackpopupmenu).  
  
##  <a name="cmfcmenubutton__m_brightarrow"></a>  CMFCMenuButton::m_bRightArrow  
 A Boolean member variable that indicates the location of the pop-up menu.  
  
```  
BOOL m_bRightArrow;  
```  
  
### Remarks  
 When the user presses the menu button, the application shows a pop-up menu. The framework will display the pop-up menu either under the button or to the right of the button. The button also has a small arrow that indicates where the pop-up menu will appear. If `m_bRightArrow` is `TRUE`, the framework displays the pop-up menu to the right of the button. Otherwise, it displays the pop-up menu under the button.  
  
##  <a name="cmfcmenubutton__m_bstaypressed"></a>  CMFCMenuButton::m_bStayPressed  
 A Boolean member variable that indicates whether the menu button appears pressed while the user makes a selection from the pop-up menu.  
  
```  
BOOL m_bStayPressed;  
```  
  
### Remarks  
 If the `m_bStayPressed` member is `FALSE`, the menu button does not become pressed when the uses clicks the button. In this case, the framework displays only the pop-up menu.  
  
 If the `m_bStayPressed` member is `TRUE`, the menu button becomes pressed when the user clicks the button. It stays pressed until after the user closes the pop-up menu, either by making a selection or canceling.  
  
##  <a name="cmfcmenubutton__m_hmenu"></a>  CMFCMenuButton::m_hMenu  
 The handle to the attached menu.  
  
```  
HMENU m_hMenu;  
```  
  
### Remarks  
 The framework displays the menu indicated by this member variable when the user clicks the menu button.  
  
##  <a name="cmfcmenubutton__m_nmenuresult"></a>  CMFCMenuButton::m_nMenuResult  
 An integer that indicates which item the user selects from the pop-up menu.  
  
```  
int m_nMenuResult;  
```  
  
### Remarks  
 The value of this member variable is zero if the user cancels the menu without making a selection or if an error occurs.  
  
##  <a name="cmfcmenubutton__pretranslatemessage"></a>  CMFCMenuButton::PreTranslateMessage  
 Called by the framework to translate window messages before they are dispatched.  
  
```  
virtual BOOL PreTranslateMessage(  
   MSG* pMsg  
);  
```  
  
### Parameters  
 [in] `pMsg`  
 Points to a [MSG](../vs140/MSG-Structure.md) structure that contains the message to process.  
  
### Return Value  
 Nonzero if the message was translated and should not be dispatched; 0 if the message was not translated and should be dispatched.  
  
### Remarks  
  
##  <a name="cmfcmenubutton__sizetocontent"></a>  CMFCMenuButton::SizeToContent  
 Changes the size of the button according to its text size and image size.  
  
```  
virtual CSize SizeToContent(  
   BOOL bCalcOnly = FALSE  
);  
```  
  
### Parameters  
 [in] `bCalcOnly`  
 A Boolean parameter that indicates whether this method resizes the button .  
  
### Return Value  
 A [CSize](../vs140/CSize-Class.md) object that specifies the new size for the button.  
  
### Remarks  
 If you call this function and `bCalcOnly` is `TRUE`, `SizeToContent` will calculate only the new size of the button.  
  
 The new size of the button is calculated to fit the button text, image, and arrow. The framework also adds in predefined margins of 10 pixels for the horizontal edge and 5 pixels for the vertical edge.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCButton Class](../vs140/CMFCButton-Class.md)