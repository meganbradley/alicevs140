---
title: "Manipulating the Tool Tip Control"
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
ms.assetid: 3600afe5-712a-4b56-8456-96e85fe879af
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Manipulating the Tool Tip Control
Class `CToolTipCtrl` provides a group of member functions that control the various attributes of the `CToolTipCtrl` object and the tool tip window.  
  
 The initial, pop-up, and reshow durations for the tool tip windows can be set and retrieved with calls to [GetDelayTime](../vs140/CToolTipCtrl--GetDelayTime.md) and [SetDelayTime](../vs140/CToolTipCtrl--SetDelayTime.md).  
  
 Change the appearance of the tool tip windows with the following functions:  
  
-   [GetMargin](../vs140/CToolTipCtrl--GetMargin.md) and [SetMargin](../vs140/CToolTipCtrl--SetMargin.md) Retrieves and sets the width between the tool tip border and the tool tip text.  
  
-   [GetMaxTipWidth](../vs140/CToolTipCtrl--GetMaxTipWidth.md) and [SetMaxTipWidth](../vs140/CToolTipCtrl--SetMaxTipWidth.md) Retrieves and sets the maximum width of the tool tip window.  
  
-   [GetTipBkColor](../vs140/CToolTipCtrl--GetTipBkColor.md) and [SetTipBkColor](../vs140/CToolTipCtrl--SetTipBkColor.md) Retrieves and sets the background color of the tool tip window.  
  
-   [GetTipTextColor](../vs140/CToolTipCtrl--GetTipTextColor.md) and [SetTipTextColor](../vs140/CToolTipCtrl--SetTipTextColor.md) Retrieves and sets the text color of the tool tip window.  
  
 In order for the tool tip control to be notified of important messages, such as **WM_LBUTTONXXX** messages, you must relay the messages to your tool tip control. The best method for this relay is to make a call to [CToolTipCtrl::RelayEvent](../vs140/CToolTipCtrl--RelayEvent.md), in the `PreTranslateMessage` function of the owner window. The following example illustrates one possible method (assuming the tool tip control is called `m_ToolTip`):  
  
 [!CODE [NVC_MFCControlLadenDialog#41](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#41)]  
  
 To immediately remove a tool tip window, call the [Pop](../vs140/CToolTipCtrl--Pop.md) member function.  
  
## See Also  
 [Using CToolTipCtrl](../vs140/Using-CToolTipCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)