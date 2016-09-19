---
title: "ToolBar Control Styles"
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
ms.assetid: 0f717eb9-fa32-4263-b852-809238863feb
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ToolBar Control Styles
[CMFCToolBarButton](../vs140/CMFCToolBarButton-Class.md) has a set of style flags that determine the appearance and behavior of the button. You can set a combination of these flags by calling [CMFCToolBarButton::SetStyles](../vs140/CMFCToolBarButton--SetStyle.md). This topic lists the style flag values and their meanings.  
  
## Property Values  
 The following values determine the type of button that the control represents:  
  
 TBBS_BUTTON  
 Standard pushbutton (default).  
  
 TBBS_CHECKBOX  
 Check box.  
  
 TBBS_CHECKGROUP  
 The start of a group of checkboxes.  
  
 TBBS_GROUP  
 The start of a group of buttons.  
  
 TBBS_SEPARATOR  
 Separator.  
  
 The following values represent the current status of the control:  
  
 TBBS_CHECKED  
 Check box is checked.  
  
 TBBS_DISABLED  
 Control is disabled.  
  
 TBBS_INDETERMINATE  
 Check box is in an indeterminate state.  
  
 TBBS_PRESSED  
 Button is pressed.  
  
 The following value changes the layout of the button in the toolbar:  
  
 TBBS_BREAK  
 Places the item on a new line or in a new column without separating columns.  
  
## Remarks  
 The current style is stored in [CMFCToolBarButton::m_nStyle](../vs140/CMFCToolBarButton--m_nStyle.md). Do not set a new value in `m_nStyle` directly, because some derived classes perform additional processing when you call `SetStyles`.  
  
 The visual manager determines the appearance of buttons in each state. See [The Visualization Manager](../vs140/Visualization-Manager.md) for more information.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CMFCToolBarButton](../vs140/CMFCToolBarButton-Class.md)   
 [The Visualization Manager](../vs140/Visualization-Manager.md)