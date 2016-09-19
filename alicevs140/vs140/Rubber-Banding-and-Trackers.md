---
title: "Rubber-Banding and Trackers"
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
ms.assetid: 0d0fa64c-6418-4baf-ab7f-2d16ca039230
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Rubber-Banding and Trackers
Another feature supplied with trackers is the "rubber-band" selection, which allows a user to select multiple OLE items by dragging a sizing rectangle around the items to be selected. When the user releases the left mouse button, items within the region selected by the user are selected and can be manipulated by the user. For instance, the user might drag the selection into another container application.  
  
 Implementing this feature requires some additional code in your application's `WM_LBUTTONDOWN` handler function.  
  
 The following code sample implements rubber-band selection and additional features.  
  
 [!CODE [NVC_MFCOClient#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOClient#6)]  
  
 If you want to allow reversible orientation of the tracker during rubber-banding, you should call [CRectTracker::TrackRubberBand](../vs140/CRectTracker--TrackRubberBand.md) with the third parameter set to **TRUE**. Remember that allowing reversible orientation will sometimes cause [CRectTracker::m_rect](../vs140/CRectTracker--m_rect.md) to become inverted. This can be corrected by a call to [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md).  
  
 For more information, see [Container Client Items](../vs140/Containers--Client-Items.md) and [Customizing Drag and Drop](../vs140/Drag-and-Drop--Customizing.md).  
  
## See Also  
 [Trackers: Implementing Trackers in Your OLE Application](../vs140/Trackers--Implementing-Trackers-in-Your-OLE-Application.md)   
 [CRectTracker Class](../vs140/CRectTracker-Class.md)