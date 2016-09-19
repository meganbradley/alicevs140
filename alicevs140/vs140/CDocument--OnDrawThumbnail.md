---
title: "CDocument::OnDrawThumbnail"
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
ms.assetid: 3efd29be-4f1f-4666-8d63-7861bd60e163
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::OnDrawThumbnail
Override this method in a derived class to draw the thumbnail.  
  
## Syntax  
  
```  
virtual void OnDrawThumbnail(  
   CDC& dc,  
   LPRECT lprcBounds  
);  
```  
  
#### Parameters  
 `dc`  
 A reference to a device context.  
  
 `lprcBounds`  
 Specifies a bounding rectangle of the area where the thumbnail should be drawn.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)