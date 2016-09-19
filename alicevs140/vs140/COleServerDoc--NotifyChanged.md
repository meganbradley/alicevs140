---
title: "COleServerDoc::NotifyChanged"
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
ms.assetid: b2264246-2b75-4aa1-b04e-d79cf5e5da8e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::NotifyChanged
Call this function to notify all linked items connected to the document that the document has changed.  
  
## Syntax  
  
```  
  
void NotifyChanged( );  
```  
  
## Remarks  
 Typically, you call this function after the user changes some global attribute such as the dimensions of the server document. If an OLE item is linked to the document with an automatic link, the item is updated to reflect the changes. In container applications written with the Microsoft Foundation Class Library, the [OnChange](../vs140/COleClientItem--OnChange.md) member function of `COleClientItem` is called.  
  
> [!NOTE]
>  This function is included for compatibility with OLE 1. New applications should use [UpdateAllItems](../vs140/COleServerDoc--UpdateAllItems.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::NotifyClosed](../vs140/COleServerDoc--NotifyClosed.md)   
 [COleServerDoc::NotifySaved](../vs140/COleServerDoc--NotifySaved.md)   
 [COleClientItem::OnChange](../vs140/COleClientItem--OnChange.md)