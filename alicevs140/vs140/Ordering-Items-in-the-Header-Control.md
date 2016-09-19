---
title: "Ordering Items in the Header Control"
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
ms.assetid: 5aaef872-75b5-49c5-8fed-6f9a81fca812
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Ordering Items in the Header Control
Once you've [added items to a header control](../vs140/Adding-Items-to-the-Header-Control.md), you can manipulate or get information about their order with the following functions:  
  
-   [CHeaderCtrl::GetOrderArray](../vs140/CHeaderCtrl--GetOrderArray.md) and [CHeaderCtrl::SetOrderArray](../vs140/CHeaderCtrl--SetOrderArray.md)  
  
     Retrieves and sets the left-to-right order of header items.  
  
-   [CHeaderCtrl::OrderToIndex](../vs140/CHeaderCtrl--OrderToIndex.md).  
  
     Retrieves the index value for a specific header item.  
  
 In addition to the previous member functions, the `HDS_DRAGDROP` style allows the user to drag and drop header items within the header control. For more information, see [Providing Drag-and-Drop Support for Header Items](../vs140/Providing-Drag-and-Drop-Support-for-Header-Items.md).  
  
## See Also  
 [Using CHeaderCtrl](../vs140/Using-CHeaderCtrl.md)