---
title: "CDocument::CDocument"
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
ms.assetid: 82eabad0-e2bd-428c-ae84-ec08b6fc8c71
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::CDocument
Constructs a **CDocument** object.  
  
## Syntax  
  
```  
  
CDocument( );  
```  
  
## Remarks  
 The framework handles document creation for you. Override the [OnNewDocument](../vs140/CDocument--OnNewDocument.md) member function to perform initialization on a per-document basis; this is particularly important in single document interface (SDI) applications.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::OnNewDocument](../vs140/CDocument--OnNewDocument.md)   
 [CDocument::OnOpenDocument](../vs140/CDocument--OnOpenDocument.md)