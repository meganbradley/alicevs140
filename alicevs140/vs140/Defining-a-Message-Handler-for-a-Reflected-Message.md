---
title: "Defining a Message Handler for a Reflected Message"
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
ms.assetid: 5a403528-58c5-46e7-90d5-4a77f0ab9b9c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Defining a Message Handler for a Reflected Message
Once you have created a new MFC control class, you can define message handlers for it. Reflected message handlers allow your control class to handle its own messages before the message is received by the parent. You can use the MFC [CWnd::SendMessage](../vs140/CWnd--SendMessage.md) function to send messages from your control to a parent window.  
  
 With this functionality you could, for example, create a list box that will redraw itself rather than relying on the parent window to do so (owner drawn). For more information on reflected messages, see [Handling Reflected Messages](../vs140/Handling-Reflected-Messages.md).  
  
 To create an [ActiveX control](../vs140/ActiveX-Controls-on-the-Internet.md) with the same functionality, you must create a project for the ActiveX control.  
  
> [!NOTE]
>  You cannot add a reflected message (OCM_*Message*) for an ActiveX control using the Properties window, as described below. You must add these messages manually.  
  
### To define a message handler for a reflected message from the Properties window  
  
1.  Add a control, such as a list, a rebar control, a toolbar, or a tree control, to your MFC project.  
  
2.  In Class View, click the name of your control class.  
  
3.  In the [Properties window](../vs140/Properties-Window.md), the control class name appears in the **Class Name** list.  
  
4.  Click the **Messages** button to display the Windows messages available to add to the control.  
  
5.  Scroll down the list of messages in the Properties window until you see the heading **Reflected**. Alternately, click the **Categories** button and collapse the view to see the **Reflected** heading.  
  
6.  Select the reflected message for which you want to define a handler. Reflected messages are marked with an equal sign (=).  
  
7.  Click the cell in the right column in the Properties window to display the suggested name of the handler as <add\>*HandlerName*. (For example, the **=WM_CTLCOLOR** message handler suggests <add\>**CtlColor**).  
  
8.  Click the suggested name to accept. The handler is added to your project.  
  
     Message handler names that you have added appear in the right column of the reflected messages window.  
  
9. To edit or delete a message handler, repeat steps 4 through 7. Click the cell containing the handler name to edit or delete and click the appropriate task.  
  
## See Also  
 [Mapping Messages to Functions](../vs140/Mapping-Messages-to-Functions.md)   
 [Adding Functionality with Code Wizards](../vs140/Adding-Functionality-with-Code-Wizards--C---.md)   
 [Adding a Class](../vs140/Adding-a-Class--Visual-C---.md)   
 [Adding a Member Function](../vs140/Adding-a-Member-Function--Visual-C---.md)   
 [Adding a Member Variable](../vs140/Adding-a-Member-Variable---Visual-C---.md)   
 [Overriding a Virtual Function](../vs140/Overriding-a-Virtual-Function--Visual-C---.md)   
 [MFC Message Handler](../vs140/Adding-an-MFC-Message-Handler.md)   
 [Navigating the Class Structure](../vs140/Navigating-the-Class-Structure--Visual-C---.md)