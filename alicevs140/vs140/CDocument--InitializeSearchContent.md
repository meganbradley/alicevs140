---
title: "CDocument::InitializeSearchContent"
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
ms.assetid: fb0b1c03-931e-416b-9a33-662de4b3ed4a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::InitializeSearchContent
Called to initialize search content for the Search Handler.  
  
## Syntax  
  
```  
virtual void InitializeSearchContent ();  
```  
  
## Remarks  
 Override this method in a derived class to initialize search content. The content should be a string with parts delimited by ";". For example, "point; rectangle; ole item".  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)