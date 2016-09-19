---
title: "User-Interface Updating for Record Views  (MFC Data Access)"
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
ms.assetid: 2c7914b6-2dc3-40c3-b2f2-8371da2a4063
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# User-Interface Updating for Record Views  (MFC Data Access)
`CRecordView` and `CDaoRecordView` also provide default user-interface update handlers for the navigation commands. These handlers automate enabling and disabling the user-interface objects — menu items and toolbar buttons. The application wizard supplies standard menus and, if you choose the **Dockable Toolbar** option, a set of toolbar buttons for the commands. If you create a record view class using `CRecordView`, you might want to add similar user-interface objects to your application.  
  
### To create menu resources with the menu editor  
  
1.  Referring to the information about using the [menu editor](../vs140/Menu-Editor.md), create your own menu with the same four commands.  
  
#### To create toolbar buttons with the graphics editor  
  
1.  Referring to the information about using the [toolbar editor](../vs140/Toolbar-Editor.md), edit the toolbar resource to add toolbar buttons for your record navigation commands.  
  
## See Also  
 [Supporting Navigation in a Record View](../vs140/Supporting-Navigation-in-a-Record-View---MFC-Data-Access-.md)   
 [Using a Record View](../vs140/Using-a-Record-View---MFC-Data-Access-.md)