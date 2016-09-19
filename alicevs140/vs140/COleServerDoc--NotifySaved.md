---
title: "COleServerDoc::NotifySaved"
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
ms.assetid: 3a591331-c22d-4f1f-b284-8e4ad61e9c16
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::NotifySaved
Call this function after the user saves the server document.  
  
## Syntax  
  
```  
  
void NotifySaved( );  
```  
  
## Remarks  
 When the user chooses the Save command from the File menu, `NotifySaved` is called for you by `COleServerDoc`'s implementation of [OnSaveDocument](../vs140/CDocument--OnSaveDocument.md). This function notifies the OLE system DLLs, which in turn notify the containers. In container applications written with the Microsoft Foundation Class Library, the [OnChange](../vs140/COleClientItem--OnChange.md) member function of `COleClientItem` is called.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::NotifyChanged](../vs140/COleServerDoc--NotifyChanged.md)   
 [COleServerDoc::NotifyClosed](../vs140/COleServerDoc--NotifyClosed.md)   
 [COleClientItem::OnChange](../vs140/COleClientItem--OnChange.md)   
 [CDocument::OnSaveDocument](../vs140/CDocument--OnSaveDocument.md)