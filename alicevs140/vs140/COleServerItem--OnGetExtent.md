---
title: "COleServerItem::OnGetExtent"
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
ms.assetid: ad5f8913-e1a7-40e2-9d55-3f8421f837db
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::OnGetExtent
Called by the framework to retrieve the size, in **HIMETRIC** units, of the OLE item.  
  
## Syntax  
  
```  
  
      virtual BOOL OnGetExtent(  
   DVASPECT nDrawAspect,  
   CSize& rSize   
);  
```  
  
#### Parameters  
 `nDrawAspect`  
 Specifies the aspect of the OLE item whose bounds are to be retrieved. This parameter can have any of the following values:  
  
-   `DVASPECT_CONTENT` Item is represented in such a way that it can be displayed as an embedded object inside its container.  
  
-   `DVASPECT_THUMBNAIL` Item is rendered in a "thumbnail" representation so that it can be displayed in a browsing tool.  
  
-   `DVASPECT_ICON` Item is represented by an icon.  
  
-   `DVASPECT_DOCPRINT` Item is represented as if it were printed using the Print command from the File menu.  
  
 `rSize`  
 Reference to a `CSize` object that will receive the size of the OLE item.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 If the container application was written with the Microsoft Foundation Class Library, this function is called when the [GetExtent](../vs140/COleClientItem--GetExtent.md) member function of the corresponding `COleClientItem` object is called. The default implementation does nothing. You must implement it yourself. Override this function if you want to perform special processing when handling a request for the size of the OLE item.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::Draw](../vs140/COleClientItem--Draw.md)   
 [COleClientItem::GetExtent](../vs140/COleClientItem--GetExtent.md)