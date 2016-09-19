---
title: "Adding an ATL Message Handler"
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
ms.assetid: cdea38a1-0d9b-4f8d-bbd5-b4f063fb3eeb
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Adding an ATL Message Handler
To add a message handler (a member function that handles Windows messages) to a control, first select the control in the Class View. Then open the **Properties** window, select the **Messages** icon, and click the drop-down control in the box opposite the required message. This will add a declaration for the message handler in the control's header file and a skeleton implementation of the handler in the control's .cpp file. It will also add the message map and add an entry for the handler.  
  
 Adding a message handler in ATL is similar to adding a message handler to an MFC class. See [Adding an MFC Message Handler](../vs140/Adding-an-MFC-Message-Handler.md) for more information.  
  
 The following conditions apply only to adding an ATL message handler:  
  
-   The message handlers follow the same naming convention as MFC.  
  
-   The new message map entries are added into the main message map. The wizard does not recognize alternate message maps and chaining.  
  
## See Also  
 [Implementing a Window](../vs140/Implementing-a-Window.md)