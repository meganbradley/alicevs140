---
title: "Tree Control Item Selection"
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
ms.assetid: 7bcb3b16-b9c8-4c06-9350-7bc3c1c5009b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Tree Control Item Selection
When the selection changes from one item to another, a tree control ([CTreeCtrl](../vs140/CTreeCtrl-Class.md)) sends [TVN_SELCHANGING](http://msdn.microsoft.com/library/windows/desktop/bb773547) and [TVN_SELCHANGED](http://msdn.microsoft.com/library/windows/desktop/bb773544) notification messages. Both notifications include a value that specifies whether the change is the result of a mouse click or a keystroke. The notifications also include information about the item that is gaining the selection and the item that is losing the selection. You can use this information to set item attributes that depend on the selection state of the item. Returning **TRUE** in response to **TVN_SELCHANGING** prevents the selection from changing; returning **FALSE** allows the change.  
  
 An application can change the selection by calling the [SelectItem](../vs140/CTreeCtrl--SelectItem.md) member function.  
  
## See Also  
 [Using CTreeCtrl](../vs140/Using-CTreeCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)