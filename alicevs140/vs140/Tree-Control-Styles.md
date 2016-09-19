---
title: "Tree Control Styles"
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
ms.assetid: f43faebd-a355-479e-888a-bf0673d5e1b4
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Tree Control Styles
Tree control ([CTreeCtrl](../vs140/CTreeCtrl-Class.md)) styles govern aspects of a tree control's appearance. You set the initial styles when you create the tree control. You can retrieve and change the styles after creating the tree control by using the [GetWindowLong](http://msdn.microsoft.com/library/windows/desktop/ms633584) and [SetWindowLong](http://msdn.microsoft.com/library/windows/desktop/ms633591) Windows functions, specifying **GWL_STYLE** for the `nIndex` parameter. For a complete list of styles, see [Tree View Control Window Styles](http://msdn.microsoft.com/library/windows/desktop/bb760013) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 The **TVS_HASLINES** style enhances the graphic representation of a tree control's hierarchy by drawing lines that link child items to their corresponding parent item. This style does not link items at the root of the hierarchy. To do so, you need to combine the **TVS_HASLINES** and **TVS_LINESATROOT** styles.  
  
 The user can expand or collapse a parent item's list of child items by double-clicking the parent item. A tree control that has the **TVS_SINGLEEXPAND** style causes the item being selected to expand and the item being unselected to collapse. If the mouse is used to single-click the selected item and that item is closed, it will be expanded. If the selected item is single-clicked when it is open, it will be collapsed.  
  
 A tree control that has the **TVS_HASBUTTONS** style adds a button to the left side of each parent item. The user can click the button to expand or collapse the child items as an alternative to double-clicking the parent item. **TVS_HASBUTTONS** does not add buttons to items at the root of the hierarchy. To do so, you must combine **TVS_HASLINES**, **TVS_LINESATROOT**, and **TVS_HASBUTTONS**.  
  
 The **TVS_EDITLABELS** style makes it possible for the user to edit the labels of tree control items. For more information about editing labels, see [Tree Control Label Editing](../vs140/Tree-Control-Label-Editing.md) later in this topic.  
  
 The **TVS_NOTOOLTIPS** style disables the automatic tool tip feature of tree view controls. This feature automatically displays a tool tip, containing the title of the item under the mouse cursor, if the entire title is not currently visible.  
  
## See Also  
 [Using CTreeCtrl](../vs140/Using-CTreeCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)