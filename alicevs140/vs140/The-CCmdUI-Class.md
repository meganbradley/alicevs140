---
title: "The CCmdUI Class"
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
ms.assetid: 2f2bae62-8c29-45a4-bbce-490eb01907d5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# The CCmdUI Class
When it routes an update command to its handler, the framework passes the handler a pointer to a `CCmdUI` object (or to an object of a `CCmdUI`-derived class). This object represents the menu item or toolbar button or other user-interface object that generated the command. The update handler calls member functions of the `CCmdUI` structure through the pointer to update the user-interface object. For example, here is an update handler for the Clear All menu item:  
  
 [!CODE [NVC_MFCDocView#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#3)]  
  
 This handler calls the **Enable** member function of an object with access to the menu item. **Enable** makes the item available for use.  
  
## See Also  
 [How to: Update User-Interface Objects](../vs140/How-to--Update-User-Interface-Objects.md)