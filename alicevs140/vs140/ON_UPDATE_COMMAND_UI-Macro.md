---
title: "ON_UPDATE_COMMAND_UI Macro"
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
ms.assetid: 3e72b50f-4119-4c82-81cf-6e09b132de05
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_UPDATE_COMMAND_UI Macro
Use the **Properties** window to connect a user-interface object to a command-update handler in a command-target object. It will automatically connect the user-interface object's ID to the `ON_UPDATE_COMMAND_UI` macro and create a handler in the object that will handle the update. See [Mapping Messages to Functions](../vs140/Mapping-Messages-to-Functions.md) for more information.  
  
 For example, to update a Clear All command in your program's Edit menu, use the **Properties** window to add a message-map entry in the chosen class, a function declaration for a command-update handler called `OnUpdateEditClearAll` in the class declaration, and an empty function template in the class's implementation file. The function prototype looks like this:  
  
 [!CODE [NVC_MFCDocView#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#2)]  
  
 Like all handlers, the function shows the **afx_msg** keyword. Like all update handlers, it takes one argument, a pointer to a `CCmdUI` object.  
  
## See Also  
 [How to: Update User-Interface Objects](../vs140/How-to--Update-User-Interface-Objects.md)