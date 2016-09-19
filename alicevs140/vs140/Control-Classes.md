---
title: "Control Classes"
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
ms.topic: article
ms.assetid: f9876606-9f5b-44cb-9135-213298d1df8f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control Classes
Control classes encapsulate a wide variety of standard Windows controls ranging from static text controls to tree controls. In addition, MFC provides some new controls, including buttons with bitmaps and control bars.  
  
 The controls whose class names end in "**Ctrl**" were new in Windows 95 and Windows NT version 3.51.  
  
## Static Display Controls  
 [CStatic](../vs140/CStatic-Class.md)  
 A static-display window. Static controls are used to label, box, or separate other controls in a dialog box or window. They may also display graphical images rather than text or a box.  
  
## Text Controls  
 [CEdit](../vs140/CEdit-Class.md)  
 An editable-text control window. Edit controls are used to accept textual input from the user.  
  
 [CIPAddressCtrl](../vs140/CIPAddressCtrl-Class.md)  
 Supports an edit box for manipulating an Internet Protocol (IP) address.  
  
 [CRichEditCtrl](../vs140/CRichEditCtrl-Class.md)  
 A control in which the user can enter and edit text. Unlike the control encapsulated in `CEdit`, a rich edit control supports character and paragraph formatting and OLE objects.  
  
## Controls That Represent Numbers  
 [CSliderCtrl](../vs140/CSliderCtrl-Class.md)  
 A control containing a slider, which the user moves to select a value or set of values.  
  
 [CSpinButtonCtrl](../vs140/CSpinButtonCtrl-Class.md)  
 A pair of arrow buttons the user can click to increment or decrement a value.  
  
 [CProgressCtrl](../vs140/CProgressCtrl-Class.md)  
 Displays a rectangle that is gradually filled from left to right to indicate the progress of an operation.  
  
 [CScrollBar](../vs140/CScrollBar-Class.md)  
 A scroll-bar control window. The class provides the functionality of a scroll bar, for use as a control in a dialog box or window, through which the user can specify a position within a range.  
  
## Buttons  
 [CButton](../vs140/CButton-Class.md)  
 A button control window. The class provides a programmatic interface for a push button, check box, or radio button in a dialog box or window.  
  
 [CBitmapButton](../vs140/CBitmapButton-Class.md)  
 A button with a bitmap rather than a text caption.  
  
## Lists  
 [CListBox](../vs140/CListBox-Class.md)  
 A list-box control window. A list box displays a list of items that the user can view and select.  
  
 [CDragListBox](../vs140/CDragListBox-Class.md)  
 Provides the functionality of a Windows list box; allows the user to move list box items, such as filenames and string literals, within the list box. List boxes with this capability are useful for an item list in an order other than alphabetical, such as include pathnames or files in a project.  
  
 [CComboBox](../vs140/CComboBox-Class.md)  
 A combo-box control window. A combo box consists of an edit control plus a list box.  
  
 [CComboBoxEx](../vs140/CComboBoxEx-Class.md)  
 Extends the combo box control by providing support for image lists.  
  
 [CCheckListBox](../vs140/CCheckListBox-Class.md)  
 Displays a list of items with check boxes, which the user can check or clear, next to each item.  
  
 [CListCtrl](../vs140/CListCtrl-Class.md)  
 Displays a collection of items, each consisting of an icon and a label, in a manner similar to the right pane of File Explorer.  
  
 [CTreeCtrl](../vs140/CTreeCtrl-Class.md)  
 Displays a hierarchical list of icons and labels arranged in a manner similar to the left pane of File Explorer.  
  
## Toolbars and Status Bars  
 [CToolBarCtrl](../vs140/CToolBarCtrl-Class.md)  
 Provides the functionality of the Windows toolbar common control. Most MFC programs use [CToolBar](../vs140/CToolBar-Class.md) instead of this class.  
  
 [CStatusBarCtrl](../vs140/CStatusBarCtrl-Class.md)  
 A horizontal window, usually divided into panes, in which an application can display status information. Most MFC programs use [CStatusBar](../vs140/CStatusBar-Class.md) instead of this class.  
  
## Miscellaneous Controls  
 [CAnimateCtrl](../vs140/CAnimateCtrl-Class.md)  
 Displays a simple video clip.  
  
 [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md)  
 A small pop-up window that displays a single line of text describing the purpose of a tool in an application.  
  
 [CDateTimeCtrl](../vs140/CDateTimeCtrl-Class.md)  
 Supports either an extended edit control, or a simple calendar interface control, that allows a user to choose a specific date or time value.  
  
 [CHeaderCtrl](../vs140/CHeaderCtrl-Class.md)  
 Displays titles or labels for columns.  
  
 [CMonthCalCtrl](../vs140/CMonthCalCtrl-Class.md)  
 Supports a simple calendar interface control that allows a user to select a date.  
  
 [CTabCtrl](../vs140/CTabCtrl-Class.md)  
 A control with tabs on which the user can click, analogous to the dividers in a notebook.  
  
 [CHotKeyCtrl](../vs140/CHotKeyCtrl-Class.md)  
 Enables the user to create a hot key combination, which the user can press to perform an action quickly.  
  
 [CLinkCtrl](../vs140/CLinkCtrl-Class.md)  
 Renders marked-up text and launches appropriate applications when the user clicks the embedded link.  
  
 [CHtmlEditCtrl](../vs140/CHtmlEditCtrl-Class.md)  
 Provides the functionality of the WebBrowser ActiveX control in an MFC window.  
  
## Related Classes  
 [CImageList](../vs140/CImageList-Class.md)  
 Provides the functionality of the Windows image list. Image lists are used with list controls and tree controls. They can also be used to store and archive a set of same-sized bitmaps.  
  
 [CCtrlView](../vs140/CCtrlView-Class.md)  
 The base class for all views associated with Windows controls. The views based on controls are described below.  
  
 [CEditView](../vs140/CEditView-Class.md)  
 A view that contains a Windows standard edit control.  
  
 [CRichEditView](../vs140/CRichEditView-Class.md)  
 A view that contains a Windows rich edit control.  
  
 [CListView](../vs140/CListView-Class.md)  
 A view that contains a Windows list control.  
  
 [CTreeView](../vs140/CTreeView-Class.md)  
 A view that contains a Windows tree control.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)