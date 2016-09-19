---
title: "CSplitButton Class"
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
ms.assetid: 6844d0a9-6408-4e44-9b5f-57628ed8bad6
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitButton Class
The `CSplitButton` class represents a split button control. The split button control performs a default behavior when a user clicks the main part of the button, and displays a drop-down menu when a user clicks the drop-down arrow of the button.  
  
## Syntax  
  
```  
class CSplitButton : public CButton  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CSplitButton::CSplitButton](#csplitbutton__csplitbutton)|Constructs a `CSplitButton` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSplitButton::Create](#csplitbutton__create)|Creates a split button control with specified styles and attaches it to the current `CSplitButton` object.|  
|[CSplitButton::SetDropDownMenu](#csplitbutton__setdropdownmenu)|Sets the drop-down menu that is displayed when a user clicks the drop-down arrow of the current split button control.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSplitButton::OnDropDown](#csplitbutton__ondropdown)|Handles the `BCN_DROPDOWN` notification that the system sends when a user clicks the drop-down arrow of the current split button control.|  
  
## Remarks  
 The `CSplitButton` class is derived from the [CButton](../vs140/CButton-Class.md) class. The split button control is a button control whose style is `BS_SPLITBUTTON`. It displays a custom menu when a user clicks the drop-down arrow. For more information, see the `BS_SPLITBUTTON` and `BS_DEFSPLITBUTTON` styles in                 [Button Styles](http://msdn.microsoft.com/library/windows/desktop/bb775951).  
  
 The following figure depicts a dialog box that contains a pager control and a (1) split button control. The (2) drop-down arrow has already been clicked and the (3) submenu is displayed.  
  
 ![Dialog with a splitbutton and pager control.](../vs140/media/SplitButton_Pager.png "SplitButton_Pager")  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CButton](../vs140/CButton-Class.md)  
  
 `CSplitButton`  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This class is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this class are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
##  <a name="csplitbutton__create"></a>  CSplitButton::Create  
 Creates a split button control with specified styles and attaches it to the current `CSplitButton` object.  
  
```  
virtual BOOL Create(  
    DWORD dwStyle,   
    const RECT& rect,   
    CWnd* pParentWnd,   
    UINT nID  
);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `dwStyle`|A bitwise combination (OR) of styles to be applied to the control. For more information, see [Button Styles](../vs140/Button-Styles.md).|  
|[in] `rect`|A reference to a                                         [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that contains the position and size of the control.|  
|[in] `pParentWnd`|A non-null pointer to a [CWnd](../vs140/CWnd-Class.md) object that is the parent window of the control.|  
|[in] `nID`|The ID of the control.|  
  
### Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
##  <a name="csplitbutton__csplitbutton"></a>  CSplitButton::CSplitButton  
 Constructs a `CSplitButton` object. The constructor's parameters specify a submenu that is displayed when a user clicks the drop-down arrow of the split button control.  
  
```  
CSplitButton();  
CSplitButton(  
    UINT nMenuId,   
    UINT nSubMenuId  
)  
CSplitButton(  
    CMenu* pMenu  
)  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `nMenuId`|The resource ID of the menu bar.|  
|[in] `nSubMenuId`|The resource ID of a submenu.|  
|[in] `pMenu`|A pointer to a [CMenu](../vs140/CMenu-Class.md) object that specifies a submenu. The `CSplitButton` object deletes the `CMenu` object and its associated `HMENU` when the `CSplitButton` object goes out of scope.|  
  
### Remarks  
 Use the [CSplitButton::Create](#csplitbutton__create) method to create a split button control and attach it to the `CSplitButton` object.  
  
##  <a name="csplitbutton__ondropdown"></a>  CSplitButton::OnDropDown  
 Handles the `BCN_DROPDOWN` notification that the system sends when a user clicks the drop-down arrow of the current split button control.  
  
```  
afx_msg void OnDropDown(  
    NMHDR* pNMHDR,   
    LRESULT* pResult  
);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `pNMHDR`|Pointer to an                                         [NMHDR](http://msdn.microsoft.com/library/windows/desktop/bb775514) structure that contains information about the                                         [BCN_DROPDOWN](http://msdn.microsoft.com/library/windows/desktop/bb775983) notification.|  
|[out] `pResult`|(Not used; no value is returned.) Return value of the                                         [BCN_DROPDOWN](http://msdn.microsoft.com/library/windows/desktop/bb775983) notification.|  
  
### Remarks  
 When the user clicks the drop-down arrow on a split button control, system sends a `BCN_DROPDOWN` notification message, which the `OnDropDown` method handles. However, the `CSplitButton` object does not forward the `BCN_DROPDOWN` notification to the control that contains the split button control. Consequently, the containing control cannot support a custom action in response to the notification.  
  
 To implement a custom action that the containing control supports, use a [CButton](../vs140/CButton-Class.md) object with a style of `BS_SPLITBUTTON` instead of a `CSplitButton` object. Then implement a handler for the `BCN_DROPDOWN` notification in the `CButton` object. For more information, see [Button Styles](../vs140/Button-Styles.md).  
  
 To implement a custom action that the split button control itself supports, use [message reflection](../vs140/TN062--Message-Reflection-for-Windows-Controls.md). Derive your own class from the `CSplitButton` class and name it, for example, CMySplitButton. Then add the following message map to your application to handle the `BCN_DROPDOWN` notification:  
  
```  
BEGIN_MESSAGE_MAP(CMySplitButton, CSplitButton)  
   ON_NOTIFY_REFLECT(BCN_DROPDOWN, &CMySplitButton::OnDropDown)  
END_MESSAGE_MAP()  
```  
  
##  <a name="csplitbutton__setdropdownmenu"></a>  CSplitButton::SetDropDownMenu  
 Sets the drop-down menu that is displayed when a user clicks the drop-down arrow of the current split button control.  
  
```  
void SetDropDownMenu(  
    UINT nMenuId,   
    UINT nSubMenuId  
);  
void SetDropDownMenu(  
    CMenu* pMenu  
);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `nMenuId`|The resource ID of the menu bar.|  
|[in] `nSubMenuId`|The resource ID of a submenu.|  
|[in] `pMenu`|Pointer to a [CMenu](../vs140/CMenu-Class.md) object that specifies a submenu. The `CSplitButton` object deletes the `CMenu` object and its associated `HMENU` when the `CSplitButton` object goes out of scope.|  
  
### Remarks  
 The `nMenuId` parameter identifies a menu bar, which is a horizontal list of menu bar items. The `nSubMenuId` parameter is a zero-based index number that identifies a submenu, which is the drop-down list of menu items associated with each menu bar item. For example, a typical application has a menu that contains the menu bar items, "File," "Edit," and "Help." The "File" menu bar item has a submenu that contains the menu items, "Open," "Close" and "Exit." When the drop-down arrow of the split-button control is clicked, the control displays the specified submenu, not the menu bar.  
  
 The following figure depicts a dialog box that contains a pager control and a (1) split button control. The (2) drop-down arrow has already been clicked and the (3) submenu is displayed.  
  
 ![Dialog with a splitbutton and pager control.](../vs140/media/SplitButton_Pager.png "SplitButton_Pager")  
  
### Example  
 The first statement in the following code example demonstrates the [CSplitButton::SetDropDownMenu](#csplitbutton__setdropdownmenu) method. We created the menu with the Visual Studio resource editor, which automatically named the menu bar ID, `IDR_MENU1`. The `nSubMenuId` parameter, which is zero, refers to the only submenu of the menu bar.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#1)]  
  
## See Also  
 [CSplitButton Class](../vs140/CSplitButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton Class](../vs140/CButton-Class.md)