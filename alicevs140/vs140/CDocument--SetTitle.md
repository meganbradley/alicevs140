---
title: "CDocument::SetTitle"
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
ms.assetid: 607a4674-c4cc-4da0-9b70-6a354605aa1a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::SetTitle
Call this function to specify the document's title (the string displayed in the title bar of a frame window).  
  
## Syntax  
  
```  
  
      virtual void SetTitle(  
   LPCTSTR lpszTitle   
);  
```  
  
#### Parameters  
 `lpszTitle`  
 Points to the string to be used as the document's title.  
  
## Remarks  
 Calling this function updates the titles of all frame windows that display the document.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::GetTitle](../vs140/CDocument--GetTitle.md)