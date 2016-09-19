---
title: "CDocument::IsSearchAndOrganizeHandler"
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
ms.assetid: 57756e0e-abc8-47d9-948c-603915a44255
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::IsSearchAndOrganizeHandler
Tells whether this instance of `CDocument` was created for the Search & Organize handler.  
  
## Syntax  
  
```  
BOOL IsSearchAndOrganizeHandler() const;  
```  
  
## Return Value  
 Returns `TRUE` if this instance of `CDocument` was created for the Search & Organize handler.  
  
## Remarks  
 Currently this function returns `TRUE` only for Rich Preview handlers implemented in an out of process server. You can set the appropriate flags (m_bPreviewHandlerMode, m_bSearchMode, m_bGetThumbnailMode) at your application level to make this function return `TRUE`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)