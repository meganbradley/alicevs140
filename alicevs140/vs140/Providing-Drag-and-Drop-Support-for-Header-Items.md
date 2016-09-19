---
title: "Providing Drag-and-Drop Support for Header Items"
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
ms.assetid: 93a152ec-804f-488f-b260-b3a438d0dc0f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Providing Drag-and-Drop Support for Header Items
To provide drag-and-drop support for header items, specify the `HDS_DRAGDROP` style. Drag-and-drop support for header items gives the user the ability to reorder the header items of a header control. The default behavior provides a semitransparent drag image of the header item being dragged and a visual indicator of the new position, if the header item is dropped.  
  
 As with common drag-and-drop functionality, you can extend the default drag-and-drop behavior by handling the **HDN_BEGINDRAG** and **HDN_ENDDRAG** notifications. You can also customize the appearance of the drag image by overriding the [CHeaderCtrl::CreateDragImage](../vs140/CHeaderCtrl--CreateDragImage.md) member function.  
  
> [!NOTE]
>  If you are providing drag-and-drop support for an embedded header control in a list control, see the Extended Style section in the [Changing List Control Styles](../vs140/Changing-List-Control-Styles.md) topic.  
  
## See Also  
 [Using CHeaderCtrl](../vs140/Using-CHeaderCtrl.md)