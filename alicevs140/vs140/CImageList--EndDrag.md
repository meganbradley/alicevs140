---
title: "CImageList::EndDrag"
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
ms.assetid: c977df15-fa69-4fca-9f7a-b49030b1fa41
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::EndDrag
Call this function to end a drag operation.  
  
## Syntax  
  
```  
  
static void PASCAL EndDrag( );  
  
```  
  
## Remarks  
 To begin a drag operation, use the `BeginDrag` member function.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#5)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::BeginDrag](../vs140/CImageList--BeginDrag.md)   
 [CImageList::Draw](../vs140/CImageList--Draw.md)   
 [CImageList::DragMove](../vs140/CImageList--DragMove.md)