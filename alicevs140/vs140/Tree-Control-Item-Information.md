---
title: "Tree Control Item Information"
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
ms.assetid: 8dcab855-27de-49e9-95d8-f78ba963ea71
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Tree Control Item Information
Tree controls ([CTreeCtrl](../vs140/CTreeCtrl-Class.md)) have a number of member functions that retrieve information about items in the control. The [GetItem](../vs140/CTreeCtrl--GetItem.md) member function retrieves some or all of the data associated with an item. This data could include the item's text, state, images, count of child items, and an application-defined 32-bit data value. There is also a [SetItem](../vs140/CTreeCtrl--SetItem.md) function that can set some or all of the data associated with an item.  
  
 The [GetItemState](../vs140/CTreeCtrl--GetItemState.md), [GetItemText](../vs140/CTreeCtrl--GetItemText.md), [GetItemData](../vs140/CTreeCtrl--GetItemData.md), and [GetItemImage](../vs140/CTreeCtrl--GetItemImage.md) member functions retrieve individual attributes of an item. Each of these functions has a corresponding Set function for setting the attributes of an item.  
  
 The [GetNextItem](../vs140/CTreeCtrl--GetNextItem.md) member function retrieves the tree control item that bears the specified relationship to the current item. This function can retrieve an item's parent, the next or previous visible item, the first child item, and so on. There are also member functions to traverse the tree: [GetRootItem](../vs140/CTreeCtrl--GetRootItem.md), [GetFirstVisibleItem](../vs140/CTreeCtrl--GetFirstVisibleItem.md), [GetNextVisibleItem](../vs140/CTreeCtrl--GetNextVisibleItem.md), [GetPrevVisibleItem](../vs140/CTreeCtrl--GetPrevVisibleItem.md), [GetChildItem](../vs140/CTreeCtrl--GetChildItem.md), [GetNextSiblingItem](../vs140/CTreeCtrl--GetNextSiblingItem.md), [GetPrevSiblingItem](../vs140/CTreeCtrl--GetPrevSiblingItem.md), [GetParentItem](../vs140/CTreeCtrl--GetParentItem.md), [GetSelectedItem](../vs140/CTreeCtrl--GetSelectedItem.md), and [GetDropHilightItem](../vs140/CTreeCtrl--GetDropHilightItem.md).  
  
 The [GetItemRect](../vs140/CTreeCtrl--GetItemRect.md) member function retrieves the bounding rectangle for a tree control item. The [GetCount](../vs140/CTreeCtrl--GetCount.md) and [GetVisibleCount](../vs140/CTreeCtrl--GetVisibleCount.md) member functions retrieve a count of the items in a tree control and a count of the items that are currently visible in the tree control's window, respectively. You can ensure that a particular item is visible by calling the [EnsureVisible](../vs140/CTreeCtrl--EnsureVisible.md) member function.  
  
## See Also  
 [Using CTreeCtrl](../vs140/Using-CTreeCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)