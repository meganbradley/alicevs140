---
title: "CDocItem::GetDocument"
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
ms.assetid: 5e0529b3-1223-4b64-9c09-5618288a1090
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocItem::GetDocument
Call this function to get the document that contains the item.  
  
## Syntax  
  
```  
  
CDocument* GetDocument( ) const;  
```  
  
## Return Value  
 A pointer to the document that contains the item; **NULL**, if the item is not part of a document.  
  
## Remarks  
 This function is overridden in the derived classes [COleClientItem](../vs140/COleClientItem-Class.md) and [COleServerItem](../vs140/COleServerItem-Class.md), returning a pointer to either a [COleDocument](../vs140/COleDocument-Class.md), a [COleLinkingDoc](../vs140/COleLinkingDoc-Class.md), or a [COleServerDoc](../vs140/COleServerDoc-Class.md) object.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CDocItem Class](../vs140/CDocItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [COleLinkingDoc Class](../vs140/COleLinkingDoc-Class.md)   
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [COleServerItem Class](../vs140/COleServerItem-Class.md)