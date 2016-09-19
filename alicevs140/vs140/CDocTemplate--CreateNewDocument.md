---
title: "CDocTemplate::CreateNewDocument"
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
ms.assetid: 1999e930-a581-4352-8a13-3c9c10b95c5b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::CreateNewDocument
Call this member function to create a new document of the type associated with this document template.  
  
## Syntax  
  
```  
  
virtual CDocument* CreateNewDocument( );  
  
```  
  
## Return Value  
 A pointer to the newly created document, or **NULL** if an error occurs.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate::CreateNewFrame](../vs140/CDocTemplate--CreateNewFrame.md)