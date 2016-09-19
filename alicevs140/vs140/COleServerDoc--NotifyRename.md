---
title: "COleServerDoc::NotifyRename"
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
ms.assetid: 227ae374-bf4f-4522-acfc-5c4c76c333a6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::NotifyRename
Call this function after the user renames the server document.  
  
## Syntax  
  
```  
  
      void NotifyRename(  
   LPCTSTR lpszNewName   
);  
```  
  
#### Parameters  
 `lpszNewName`  
 Pointer to a string specifying the new name of the server document; this is typically a fully qualified path.  
  
## Remarks  
 When the user chooses the Save As command from the File menu, `NotifyRename` is called by `COleServerDoc`'s implementation of the [OnSaveDocument](../vs140/CDocument--OnSaveDocument.md) member function. This function notifies the OLE system DLLs, which in turn notify the containers. In container applications written with the Microsoft Foundation Class Library, the [OnChange](../vs140/COleClientItem--OnChange.md) member function of `COleClientItem` is called.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::NotifySaved](../vs140/COleServerDoc--NotifySaved.md)   
 [CDocument::OnSaveDocument](../vs140/CDocument--OnSaveDocument.md)