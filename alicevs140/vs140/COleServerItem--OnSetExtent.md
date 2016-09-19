---
title: "COleServerItem::OnSetExtent"
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
ms.assetid: ea3af58a-198a-4d43-b864-115075333007
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::OnSetExtent
Called by the framework to tell the OLE item how much space is available to it in the container document.  
  
## Syntax  
  
```  
  
      virtual BOOL OnSetExtent(  
   DVASPECT nDrawAspect,  
   const CSize& size   
);  
```  
  
#### Parameters  
 `nDrawAspect`  
 Specifies the aspect of the OLE item whose bounds are being specified. This parameter can have any of the following values:  
  
-   `DVASPECT_CONTENT` Item is represented in such a way that it can be displayed as an embedded object inside its container.  
  
-   `DVASPECT_THUMBNAIL` Item is rendered in a "thumbnail" representation so that it can be displayed in a browsing tool.  
  
-   `DVASPECT_ICON` Item is represented by an icon.  
  
-   `DVASPECT_DOCPRINT` Item is represented as if it were printed using the Print command from the File menu.  
  
 `size`  
 A [CSize](../vs140/CSize-Class.md) structure specifying the new size of the OLE item.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 If the container application was written with the Microsoft Foundation Class Library, this function is called when the [SetExtent](../vs140/COleClientItem--SetExtent.md) member function of the corresponding `COleClientItem` object is called. The default implementation sets the [m_sizeExtent](../vs140/COleServerItem--m_sizeExtent.md) member to the specified size if `nDrawAspect` is `DVASPECT_CONTENT`; otherwise it returns 0. Override this function to perform special processing when you change the size of the item.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::SetExtent](../vs140/COleClientItem--SetExtent.md)   
 [COleServerItem::OnGetExtent](../vs140/COleServerItem--OnGetExtent.md)   
 [COleServerItem::m_sizeExtent](../vs140/COleServerItem--m_sizeExtent.md)