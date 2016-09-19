---
title: "Controls (MFC)"
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
ms.assetid: b2842884-6435-4b8f-933b-21671bf8af95
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Controls (MFC)
Controls are objects that users can interact with to enter or manipulate data. They commonly appear in dialog boxes or on toolbars. This topic family covers three main kinds of controls:  
  
-   Windows common controls, including owner-drawn controls  
  
-   ActiveX Controls  
  
-   Other control classes supplied by the Microsoft Foundation Class Library (MFC)  
  
## Windows Common Controls  
 The Windows operating system has always provided a number of Windows common controls. These control objects are programmable, and the Visual C++ dialog editor supports adding them to your dialog boxes. The Microsoft Foundation Class Library (MFC) supplies classes that encapsulate each of these controls, as shown in the table [Windows Common Controls and MFC Classes](#_core_windows_common_controls_and_mfc_classes). (Some items in the table have related topics that describe them further. For controls that lack topics, see the documentation for the MFC class.)  
  
 Class [CWnd](../vs140/CWnd-Class.md) is the base class of all window classes, including all of the control classes. The Windows common controls are supported in the following environments:  
  
-   Windows 95, Windows 98, and Windows 2000  
  
-   Windows NT, version 3.51 and later  
  
-   Win32s, version 1.3 (Visual C++ versions 4.2 and later do not support Win32s)  
  
 The older common controls — check boxes, combo boxes, edit boxes, list boxes, option buttons, pushbuttons, scroll bar controls, and static controls — were available in earlier versions of Windows as well.  
  
## ActiveX Controls  
 ActiveX controls, formerly known as OLE controls, can be used in dialog boxes in your applications for Windows, or in HTML pages on the World Wide Web. For more information, see [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md).  
  
## Other MFC Control Classes  
 In addition to classes that encapsulate all of the Windows common controls and that support programming your own ActiveX controls (or using ActiveX controls supplied by others), MFC supplies the following control classes of its own:  
  
-   [CBitmapButton](../vs140/CBitmapButton-Class.md)  
  
-   [CCheckListBox](../vs140/CCheckListBox-Class.md)  
  
-   [CDragListBox](../vs140/CDragListBox-Class.md)  
  
##  <a name="_core_finding_information_about_windows_common_controls"></a> Finding Information About Windows Common Controls  
 The table below briefly describes each of the Windows common controls, including the control's MFC wrapper class.  
  
### Windows Common Controls and MFC Classes  
  
|Control|MFC class|Description|New in Windows 95?|  
|-------------|---------------|-----------------|------------------------|  
|[animation](../vs140/Using-CAnimateCtrl.md)|[CAnimateCtrl](../vs140/CAnimateCtrl-Class.md)|Displays successive frames of an AVI video clip|Yes|  
|button|[CButton](../vs140/CButton-Class.md)|Pushbuttons that cause an action; also used for check boxes, radio buttons, and group boxes|No|  
|combo box|[CComboBox](../vs140/CComboBox-Class.md)|Combination of an edit box and a list box|No|  
|[date and time picker](../vs140/Using-CDateTimeCtrl.md)|[CDateTimeCtrl](../vs140/CDateTimeCtrl-Class.md)|Allows the user to choose a specific date or time value|Yes|  
|edit box|[CEdit](../vs140/CEdit-Class.md)|Boxes for entering text|No|  
|[extended combo box](../vs140/Using-CComboBoxEx.md)|[CComboBoxEx](../vs140/CComboBoxEx-Class.md)|A combo box control with the ability to display images|Yes|  
|[header](../vs140/Using-CHeaderCtrl.md)|[CHeaderCtrl](../vs140/CHeaderCtrl-Class.md)|Button that appears above a column of text; controls width of text displayed|Yes|  
|[hotkey](../vs140/Using-CHotKeyCtrl.md)|[CHotKeyCtrl](../vs140/CHotKeyCtrl-Class.md)|Window that enables user to create a "hot key" to perform an action quickly|Yes|  
|[image list](../vs140/Using-CImageList.md)|[CImageList](../vs140/CImageList-Class.md)|Collection of images used to manage large sets of icons or bitmaps (image list isn't really a control; it supports lists used by other controls)|Yes|  
|[list](../vs140/Using-CListCtrl.md)|[CListCtrl](../vs140/CListCtrl-Class.md)|Window that displays a list of text with icons|Yes|  
|list box|[CListBox](../vs140/CListBox-Class.md)|Box that contains a list of strings|No|  
|[month calendar](../vs140/Using-CMonthCalCtrl.md)|[CMonthCalCtrl](../vs140/CMonthCalCtrl-Class.md)|Control that displays date information|Yes|  
|[progress](../vs140/Using-CProgressCtrl.md)|[CProgressCtrl](../vs140/CProgressCtrl-Class.md)|Window that indicates progress of a long operation|Yes|  
|[rebar](../vs140/Using-CReBarCtrl.md)|[CRebarCtrl](../vs140/CReBarCtrl-Class.md)|Tool bar that can contain additional child windows in the form of controls|Yes|  
|[rich edit](../vs140/Using-CRichEditCtrl.md)|[CRichEditCtrl](../vs140/CRichEditCtrl-Class.md)|Window in which user can edit with character and paragraph formatting (see [Classes Related to Rich Edit Controls](../vs140/Classes-Related-to-Rich-Edit-Controls.md))|Yes|  
|scroll bar|[CScrollBar](../vs140/CScrollBar-Class.md)|Scroll bar used as a control inside a dialog box (not on a window)|No|  
|[slider](../vs140/Using-CSliderCtrl.md)|[CSliderCtrl](../vs140/CSliderCtrl-Class.md)|Window containing a slider control with optional tick marks|Yes|  
|[spin button](../vs140/Using-CSpinButtonCtrl.md)|[CSpinButtonCtrl](../vs140/CSpinButtonCtrl-Class.md)|Pair of arrow buttons user can click to increment or decrement a value|Yes|  
|static-text|[CStatic](../vs140/CStatic-Class.md)|Text for labeling other controls|No|  
|[status bar](../vs140/Using-CStatusBarCtrl.md)|[CStatusBarCtrl](../vs140/CStatusBarCtrl-Class.md)|Window for displaying status information, similar to MFC class `CStatusBar`|Yes|  
|[tab](../vs140/Using-CTabCtrl.md)|[CTabCtrl](../vs140/CTabCtrl-Class.md)|Analogous to the dividers in a notebook; used in "tab dialog boxes" or property sheets|Yes|  
|[toolbar](../vs140/Using-CToolBarCtrl.md)|[CToolBarCtrl](../vs140/CToolBarCtrl-Class.md)|Window with command-generating buttons, similar to MFC class `CToolBar`|Yes|  
|[tool tip](../vs140/Using-CToolTipCtrl.md)|[CToolTipCtrl](../vs140/CToolTipCtrl-Class.md)|Small pop-up window that describes purpose of a toolbar button or other tool|Yes|  
|[tree](../vs140/Using-CTreeCtrl.md)|[CTreeCtrl](../vs140/CTreeCtrl-Class.md)|Window that displays a hierarchical list of items|Yes|  
  
### What do you want to know more about?  
  
-   An individual control: see the table [Windows Common Controls and MFC Classes](#_core_windows_common_controls_and_mfc_classes) in this topic for links to all controls  
  
-   [Making and using controls](../vs140/Making-and-Using-Controls.md)  
  
-   [Using the dialog editor to add controls](../vs140/Using-the-Dialog-Editor-to-Add-Controls.md)  
  
-   [Adding controls to a dialog box by hand](../vs140/Adding-Controls-By-Hand.md)  
  
-   [Deriving control classes from the MFC control classes](../vs140/Deriving-Controls-from-a-Standard-Control.md)  
  
-   [Using common controls as child windows](../vs140/Using-a-Common-Control-as-a-Child-Window.md)  
  
-   [Notifications from common controls](../vs140/Receiving-Notification-from-Common-Controls.md)  
  
-   [Add common controls to a dialog box](../vs140/Using-Common-Controls-in-a-Dialog-Box.md).  
  
-   [Derive a control from a standard Windows control](../vs140/Deriving-Controls-from-a-Standard-Control.md)  
  
-   [Access dialog-box controls with type safety](../vs140/Type-Safe-Access-to-Controls-in-a-Dialog-Box.md)  
  
-   [Receive notification messages from common controls](../vs140/Receiving-Notification-from-Common-Controls.md)  
  
-   [Samples](../vs140/Common-Control-Sample-List.md)  
  
 For information about Windows common controls in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)], see [Common Controls](http://msdn.microsoft.com/library/windows/desktop/bb775493).  
  
## See Also  
 [User Interface Elements](../vs140/User-Interface-Elements--MFC-.md)   
 [Dialog Editor](../vs140/Dialog-Editor.md)