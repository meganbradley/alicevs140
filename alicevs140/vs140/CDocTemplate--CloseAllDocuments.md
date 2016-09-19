---
title: "CDocTemplate::CloseAllDocuments"
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
ms.assetid: c595e003-3d8f-4fb0-93ca-14f4130ee22b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::CloseAllDocuments
Call this member function to close all open documents.  
  
## Syntax  
  
```  
  
      virtual void CloseAllDocuments(  
   BOOL bEndSession   
);  
```  
  
#### Parameters  
 `bEndSession`  
 Specifies whether or not the session is being ended. It is **TRUE** if the session is being ended; otherwise **FALSE**.  
  
## Remarks  
 This member function is typically used as part of the File Exit command. The default implementation of this function calls the [CDocument::DeleteContents](../vs140/CDocument--DeleteContents.md) member function to delete the document's data and then closes the frame windows for all the views attached to the document.  
  
 Override this function if you want to require the user to perform special cleanup processing before the document is closed. For example, if the document represents a record in a database, you may want to override this function to close the database.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate::OpenDocumentFile](../vs140/CDocTemplate--OpenDocumentFile.md)   
 [CDocTemplate::SaveAllModified](../vs140/CDocTemplate--SaveAllModified.md)