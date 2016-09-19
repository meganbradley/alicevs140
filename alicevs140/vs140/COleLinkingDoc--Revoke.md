---
title: "COleLinkingDoc::Revoke"
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
ms.assetid: b51f340b-13f3-46e7-b93d-a92708d03acf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleLinkingDoc::Revoke
Informs the OLE system DLLs that the document is no longer open.  
  
## Syntax  
  
```  
  
void Revoke( );  
```  
  
## Remarks  
 Call this function to revoke the document's registration with the OLE system DLLs.  
  
 You should call this function when closing a named file, but you usually do not need to call it directly. `Revoke` is called for you by `COleLinkingDoc`'s implementation of `OnCloseDocument`, `OnNewDocument`, `OnOpenDocument`, and `OnSaveDocument`.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleLinkingDoc Class](../vs140/COleLinkingDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleTemplateServer Class](../vs140/COleTemplateServer-Class.md)   
 [CDocument::OnCloseDocument](../vs140/CDocument--OnCloseDocument.md)   
 [CDocument::OnNewDocument](../vs140/CDocument--OnNewDocument.md)   
 [CDocument::OnOpenDocument](../vs140/CDocument--OnOpenDocument.md)   
 [CDocument::OnSaveDocument](../vs140/CDocument--OnSaveDocument.md)