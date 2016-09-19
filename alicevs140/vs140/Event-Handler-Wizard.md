---
title: "Event Handler Wizard"
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
ms.assetid: af8e1835-94b1-4d9a-b353-c519e011d3a1
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event Handler Wizard
This wizard adds an event handler for a dialog box control to the class of your choice. If you add an event handler from the [Properties window](../vs140/Properties-Window.md), you can add it only to the class that implements the dialog box. See [Adding Event Handlers for Dialog Box Controls](../vs140/Adding-Event-Handlers-for-Dialog-Box-Controls.md) for more information.  
  
 **Command name**  
 Identifies the selected control, for which the event handler is added. This box is unavailable.  
  
 **Message type**  
 Displays the list of current possible message handlers for the selected control.  
  
 **Function handler name**  
 Displays the name of the function that is added to handle the event. By default, the name is based on the message type and the command, prepended by "On". For example, for the button called `IDC_BUTTON1`, the message type `BN_CLICKED` displays the function handler name `OnBnClickedButton1`.  
  
 **Class list**  
 Displays available classes to which you can add an event handler. The class for the selected dialog box is displayed in red.  
  
 **Handler description**  
 Provides a description for the item selected in the **Message type** box. This box is unavailable.  
  
 **Add and edit**  
 Adds the message handler to the selected class or object, and then opens the text editor to the new function so you can add the control notification handler code.  
  
 **Edit code**  
 Opens the text editor to the selected existing function so you can add or edit the control notification handler code.  
  
## See Also  
 [Adding an Event Handler](../vs140/Adding-an-Event-Handler--Visual-C---.md)