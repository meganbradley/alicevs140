---
title: "CDocument::SaveModified"
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
ms.assetid: 1ef1a570-8cb6-4995-b69c-b373bc47883e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::SaveModified
Called by the framework before a modified document is to be closed.  
  
## Syntax  
  
```  
  
virtual BOOL SaveModified( );  
```  
  
## Return Value  
 Nonzero if it is safe to continue and close the document; 0 if the document should not be closed.  
  
## Remarks  
 The default implementation of this function displays a message box asking the user whether to save the changes to the document, if any have been made. Override this function if your program requires a different prompting procedure. This is an advanced overridable.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::CanCloseFrame](../vs140/CDocument--CanCloseFrame.md)   
 [CDocument::IsModified](../vs140/CDocument--IsModified.md)   
 [CDocument::OnNewDocument](../vs140/CDocument--OnNewDocument.md)   
 [CDocument::OnOpenDocument](../vs140/CDocument--OnOpenDocument.md)   
 [CDocument::OnSaveDocument](../vs140/CDocument--OnSaveDocument.md)