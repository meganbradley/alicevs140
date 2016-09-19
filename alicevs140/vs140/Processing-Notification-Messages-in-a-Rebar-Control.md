---
title: "Processing Notification Messages in a Rebar Control"
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
ms.assetid: 40f43a60-0c18-4d8d-8fab-213a095624f9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Processing Notification Messages in a Rebar Control
In the parent class of the rebar control, create an `OnChildNotify` handler function with a switch statement for any rebar-control (`CReBarCtrl`) notification messages you want to handle. Notifications are sent to the parent window when the user drags objects over the rebar control, changes the layout of the rebar bands, deletes bands from the rebar control, and so on.  
  
 The following notification messages can be sent by the rebar control object:  
  
-   **RBN_AUTOSIZE** Sent by a rebar control (created with the **RBS_AUTOSIZE** style) when the rebar automatically resizes itself.  
  
-   **RBN_BEGINDRAG** Sent by a rebar control when the user begins dragging a band.  
  
-   **RBN_CHILDSIZE** Sent by a rebar control when a band's child window is resized.  
  
-   **RBN_DELETEDBAND** Sent by a rebar control after a band has been deleted.  
  
-   **RBN_DELETINGBAND** Sent by a rebar control when a band is about to be deleted.  
  
-   **RBN_ENDDRAG** Sent by a rebar control when the user stops dragging a band.  
  
-   **RBN_GETOBJECT** Sent by a rebar control (created with the **RBS_REGISTERDROP** style) when an object is dragged over a band in the control.  
  
-   **RBN_HEIGHTCHANGE** Sent by a rebar control when its height has changed.  
  
-   **RBN_LAYOUTCHANGED** Sent by a rebar control when the user changes the layout of the control's bands.  
  
 For more information on these notifications, see [Rebar Control Reference](http://msdn.microsoft.com/library/windows/desktop/bb774375) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [Using CReBarCtrl](../vs140/Using-CReBarCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)