---
title: "COleServerItem::OnDraw"
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
ms.assetid: ad067114-1b09-4e78-9b42-839034c66f75
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::OnDraw
Called by the framework to render the OLE item into a metafile.  
  
## Syntax  
  
```  
  
      virtual BOOL OnDraw(  
   CDC* pDC,  
   CSize& rSize   
) = 0;  
```  
  
#### Parameters  
 `pDC`  
 A pointer to the [CDC](../vs140/CDC-Class.md) object on which to draw the item. The display context is automatically connected to the attribute display context so you can call attribute functions, although doing so would make the metafile device-specific.  
  
 `rSize`  
 Size, in **HIMETRIC** units, in which to draw the metafile.  
  
## Return Value  
 Nonzero if the item was successfully drawn; otherwise 0.  
  
## Remarks  
 The metafile representation of the OLE item is used to display the item in the container application. If the container application was written with the Microsoft Foundation Class Library, the metafile is used by the [Draw](../vs140/COleClientItem--Draw.md) member function of the corresponding [COleClientItem](../vs140/COleClientItem-Class.md) object. There is no default implementation. You must override this function to draw the item into the device context specified.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::Draw](../vs140/COleClientItem--Draw.md)