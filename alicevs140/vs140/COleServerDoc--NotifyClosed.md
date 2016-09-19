---
title: "COleServerDoc::NotifyClosed"
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
ms.assetid: 51063268-6f98-4ffa-89dc-27e8903234b2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::NotifyClosed
Call this function to notify the container(s) that the document has been closed.  
  
## Syntax  
  
```  
  
void NotifyClosed( );  
```  
  
## Remarks  
 When the user chooses the Close command from the File menu, `NotifyClosed` is called by `COleServerDoc`'s implementation of the [OnCloseDocument](../vs140/CDocument--OnCloseDocument.md) member function. In container applications written with the Microsoft Foundation Class Library, the [OnChange](../vs140/COleClientItem--OnChange.md) member function of `COleClientItem` is called.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::NotifyChanged](../vs140/COleServerDoc--NotifyChanged.md)   
 [COleServerDoc::NotifySaved](../vs140/COleServerDoc--NotifySaved.md)   
 [COleClientItem::OnChange](../vs140/COleClientItem--OnChange.md)   
 [CDocument::OnCloseDocument](../vs140/CDocument--OnCloseDocument.md)