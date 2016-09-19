---
title: "Trackers"
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
ms.assetid: dcd09399-6637-4621-80e5-d12670429787
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Trackers
The [CRectTracker](../vs140/CRectTracker-Class.md) class provides a user interface between rectangular items in your application and your user by providing a variety of display styles. These styles include solid, hatched, or dashed borders; a hatched pattern that covers the item; and resize handles that can be located on the outside or inside of a border. Trackers are often used in conjunction with OLE items, that is, objects derived from `COleClientItem`. The tracker rectangles give visual cues on the current status of the item.  
  
 The MFC OLE sample [OCLIENT](../vs140/Visual-C---Samples.md) demonstrates a common interface using trackers and OLE client items from the viewpoint of a container application. For a demonstration of the different styles and abilities of a tracker object, see the MFC general sample [TRACKER](../vs140/Visual-C---Samples.md).  
  
 For more information on implementing trackers in your OLE application, see [Trackers: Implementing Trackers in Your OLE Application](../vs140/Trackers--Implementing-Trackers-in-Your-OLE-Application.md)  
  
## See Also  
 [OLE](../vs140/OLE-in-MFC.md)   
 [COleClientItem Class](../vs140/COleClientItem-Class.md)