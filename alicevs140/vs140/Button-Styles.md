---
title: "Button Styles"
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
ms.assetid: 41206f72-2b92-4250-ae32-31184046402f
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Button Styles
This topic describes button types and styles.  
  
## Button Types  
 The following table lists button types. You can optionally choose one of the following. If you do not specify a button type, the default is `BS_PUSHBUTTON`.  
  
|Type|Description|  
|----------|-----------------|  
|`BS_3STATE`|Creates a check box button with three states: `BST_CHECKED`, `BST_INDETERMINATE`, and `BST_UNCHECKED`. Clicking on the button sends a `BN_CLICKED` notification to the owner window but does not change the state of the button. By default, associated text is displayed to the right of the check box. To display text to the left of the check box, use the `BS_LEFTTEXT` or `BS_RIGHTBUTTON` style.|  
|`BS_AUTO3STATE`|Creates a check box button with three states: `BST_CHECKED`, `BST_INDETERMINATE`, and `BST_UNCHECKED`. Clicking on the button sends a `BN_CLICKED` notification to the owner window and changes the state of the button. The button states cycle in the order of `BST_CHECKED`, `BST_INDETERMINATE`, and `BST_UNCHECKED`. By default, associated text is displayed to the right of the check box. To display text to the left of the check box, use the `BS_LEFTTEXT` or `BS_RIGHTBUTTON` style.|  
|`BS_AUTOCHECKBOX`|Creates a check box button with two states: `BST_CHECKED` and `BST_UNCHECKED`. Clicking on the button sends a `BN_CLICKED` notification to the owner window and changes the state of the button. By default, associated text is displayed to the right of the check box. To display text to the left of the check box, use the `BS_LEFTTEXT` or `BS_RIGHTBUTTON` style.|  
|`BS_AUTORADIOBUTTON`|Creates a radio button with two states: `BST_CHECKED` and `BST_UNCHECKED`. Radio buttons are usually used in groups, with each group having a maximum of one checked option at a time. Clicking on the button sends a `BN_CLICKED` notification to the owner window, sets the state of the clicked radio button to `BST_CHECKED`, and sets the states of all other radio buttons in the button group to `BST_UNCHECKED`. By default, associated text is displayed to the right of the radio button. To display text to the left of the radio button, use the `BS_LEFTTEXT` or `BS_RIGHTBUTTON` style.|  
|`BS_CHECKBOX`|Creates a check box button with two states: `BST_CHECKED` and `BST_UNCHECKED`. Clicking on the button sends a `BN_CLICKED` notification to the owner window but does not change the state of the button. By default, associated text is displayed to the right of the check box. To display text to the left of the check box, use the `BS_LEFTTEXT` or `BS_RIGHTBUTTON` style.|  
|`BS_COMMANDLINK`|Creates a command link button. A command link button is a command button specific to [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] that displays a green arrow to the left of the main text and a note below the main text. You can set the note text using [CButton::SetNote](../vs140/CButton--SetNote.md).|  
|`BS_DEFCOMMANDLINK`|Creates a command link button. A command link button is a command button specific to [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] that displays a green arrow to the left of the main text and a note below the main text. You can set the note text using [CButton::SetNote](../vs140/CButton--SetNote.md). If the button is in a dialog box, pressing the ENTER key sends a `BN_CLICKED` notification to the dialog box even when the button does not have the input focus.|  
|`BS_DEFPUSHBUTTON`|Creates a command button that has a heavy black border. If the button is in a dialog box, pressing the ENTER key sends a `BN_CLICKED` notification to the dialog box even when the button does not have the input focus.|  
|`BS_DEFSPLITBUTTON`|Creates a split button. A split button is a command button specific to [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] that contains a button adjacent to a drop-down arrow. When you click the button, the default command is executed. When you click the drop-down arrow, a menu of additional commands appears. If the split button is in a dialog box, pressing the ENTER key sends a `BN_CLICKED` notification to the dialog box even when the button does not have the input focus|  
|`BS_GROUPBOX`|Creates a rectangle in which other buttons can be grouped. Text associated with this style is displayed in the rectangle's upper-left corner.|  
|`BS_OWNERDRAW`|Creates an owner-drawn button. The framework calls the `DrawItem` method when a visual aspect of the button has changed. This style must be set when you use the `CBitmapButton` class.|  
|`BS_PUSHBUTTON`|Creates a command button that sends a `BN_CLICKED` notification to the owner window when the user clicks the button.|  
|`BS_RADIOBUTTON`|Creates a radio button with two states: `BST_CHECKED` and `BST_UNCHECKED`. Radio buttons are usually used in groups, with each group having a maximum of one checked option at a time. Clicking on the button sends a `BN_CLICKED` notification to the owner window but does not automatically change the state of any button in the group. By default, associated text is displayed to the right of the radio button. To display text to the left of the radio button, use the `BS_LEFTTEXT` or `BS_RIGHTBUTTON` style.|  
|`BS_SPLITBUTTON`|Creates a split button. A split button is a command button specific to [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] that contains a button adjacent to a drop-down arrow. When you click the button, the default command is executed. When you click the drop-down arrow, a menu of additional commands appears.|  
|`BS_USERBUTTON`|Obsolete, but provided for compatibility with 16-bit versions of Windows. Win32-based applications should use `BS_OWNERDRAW` instead.|  
  
## Radio Button and Check Box Styles  
 The following table lists styles that are specific to radio buttons and check boxes. These styles are ignored in all other button types. You can optionally choose one or more of the following.  
  
|Style|Description|  
|-----------|-----------------|  
|`BS_LEFTTEXT`|When combined with a radio button or check-box style, the text appears on the left side of the radio button or check box.|  
|`BS_RIGHTBUTTON`|When combined with a radio button or check-box style, the text appears on the left side of the radio button or check box. This style is identical to the `BS_LEFTTEXT` style.|  
|`BS_PUSHLIKE`|Makes a check box or radio button look and behave like a command button. The button appears pressed when its state is `BST_CHECKED`, pressed and dimmed when its state is `BST_INDETERMINATE`, and released when its state is `BST_UNCHECKED`.|  
  
## Text Alignment Styles  
 The following table lists horizontal and vertical text alignment options. You can optionally choose one of the following.  
  
|Style|Description|  
|-----------|-----------------|  
|`BS_LEFT`|Left aligns the text in the button rectangle. However, if the button is a check box or radio button that does not have the `BS_RIGHTBUTTON` style, the text is left aligned on the right side of the check box or radio button.|  
|`BS_RIGHT`|Right aligns the text in the button rectangle. However, if the button is a check box or radio button that does not have the `BS_RIGHTBUTTON` style, the text is right aligned on the right side of the check box or radio button.|  
|`BS_CENTER`|Centers text horizontally in the button rectangle.|  
|`BS_TOP`|Places text at the top of the button rectangle.|  
|`BS_BOTTOM`|Places text at the bottom of the button rectangle.|  
|`BS_VCENTER`|Centers text vertically in the button rectangle.|  
  
## Button Content Options  
 The following table lists options that indicate what is displayed in the button. Button types that only display text ignore these styles. You can optionally choose one of the following.  
  
|Style|Description|  
|-----------|-----------------|  
|`BS_BITMAP`|Specifies that the button displays a bitmap.|  
|`BS_ICON`|Specifies that the button displays an icon.|  
|`BS_TEXT`|Specifies that the button displays text.|  
  
## Other Options  
 The following table lists additional options that you can use with any button type. You can optionally choose one or more of the following.  
  
|Style|Description|  
|-----------|-----------------|  
|`BS_FLAT`|Specifies that the button is two-dimensional and is not drawn with default shading to create a three-dimensional image.|  
|`BS_MULTILINE`|Wraps the button text to multiple lines if the text string is too long to fit on a single line in the button rectangle.|  
|`BS_NOTIFY`|Enables a button to send `BN_DBLCLK`, `BN_KILLFOCUS`, and `BN_SETFOCUS` notification messages to its parent window. Note that buttons send the `BN_CLICKED` notification regardless of whether this style is specified.|  
  
## See Also  
 [Styles Used by MFC](../vs140/Styles-Used-by-MFC.md)   
 [CButton::Create](../vs140/CButton--Create.md)   
 [Button Styles](http://msdn.microsoft.com/library/windows/desktop/bb775951)   
 [BN_CLICKED Notification](_win32_bn_clicked_notification)