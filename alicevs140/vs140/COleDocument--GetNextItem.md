---
title: "COleDocument::GetNextItem"
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
ms.assetid: ff091181-66a7-483a-9d5d-2710e0efcd53
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::GetNextItem
Call this function repeatedly to access each of the items in your document.  
  
## Syntax  
  
```  
  
      virtual CDocItem* GetNextItem(  
   POSITION& pos   
) const;   
```  
  
#### Parameters  
 `pos`  
 A reference to a **POSITION** value set by a previous call to `GetNextItem`; the initial value is returned by the `GetStartPosition` member function.  
  
## Return Value  
 A pointer to the document item at the specified position.  
  
## Remarks  
 After each call, the value of `pos` is set to the **POSITION** value of the next item in the document. If the retrieved element is the last element in the document, the new value of `pos` is **NULL**.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#2)]  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument::GetStartPosition](../vs140/COleDocument--GetStartPosition.md)   
 [COleDocument::GetNextClientItem](../vs140/COleDocument--GetNextClientItem.md)   
 [COleDocument::GetNextServerItem](../vs140/COleDocument--GetNextServerItem.md)