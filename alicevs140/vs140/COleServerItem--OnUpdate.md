---
title: "COleServerItem::OnUpdate"
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
ms.topic: reference
ms.assetid: 3de50225-5db9-4f3e-843c-fe1c963b54cd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::OnUpdate
Called by the framework when an item has been modified.  
  
## Syntax  
  
```  
  
      virtual void OnUpdate(  
   COleServerItem* pSender,  
   LPARAM lHint,  
   CObject* pHint,  
   DVASPECT nDrawAspect   
);  
```  
  
#### Parameters  
 `pSender`  
 Pointer to the item that modified the document. Can be **NULL**.  
  
 `lHint`  
 Contains information about the modification.  
  
 `pHint`  
 Pointer to an object storing information about the modification.  
  
 `nDrawAspect`  
 A value from the `DVASPECT` enumeration. This parameter can have any one of the following values:  
  
-   `DVASPECT_CONTENT` Item is represented in such a way that it can be displayed as an embedded object inside its container.  
  
-   `DVASPECT_THUMBNAIL` Item is rendered in a "thumbnail" representation so that it can be displayed in a browsing tool.  
  
-   `DVASPECT_ICON` Item is represented by an icon.  
  
-   `DVASPECT_DOCPRINT` Item is represented as if it were printed using the Print command from the File menu.  
  
## Remarks  
 The default implementation calls [NotifyChanged](../vs140/COleServerItem--NotifyChanged.md), regardless of the hint or sender.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::NotifyChanged](../vs140/COleServerItem--NotifyChanged.md)