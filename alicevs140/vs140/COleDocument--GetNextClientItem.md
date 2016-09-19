---
title: "COleDocument::GetNextClientItem"
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
ms.assetid: c094e1a6-69b3-49cd-a062-e90f6decdf68
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::GetNextClientItem
Call this function repeatedly to access each of the client items in your document.  
  
## Syntax  
  
```  
  
      COleClientItem* GetNextClientItem(  
   POSITION& pos   
) const;  
```  
  
#### Parameters  
 `pos`  
 A reference to a **POSITION** value set by a previous call to `GetNextClientItem`; the initial value is returned by the `GetStartPosition` member function.  
  
## Return Value  
 A pointer to the next client item in the document, or **NULL** if there are no more client items.  
  
## Remarks  
 After each call, the value of `pos` is set for the next item in the document, which might or might not be a client item.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#1)]  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [COleDocument::GetStartPosition](../vs140/COleDocument--GetStartPosition.md)   
 [COleDocument::GetNextServerItem](../vs140/COleDocument--GetNextServerItem.md)   
 [COleDocument::GetNextItem](../vs140/COleDocument--GetNextItem.md)