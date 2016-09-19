---
title: "COleDocument::GetNextServerItem"
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
ms.assetid: c33c44bc-8eda-4d3c-9d76-b88d0c96d0a9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::GetNextServerItem
Call this function repeatedly to access each of the server items in your document.  
  
## Syntax  
  
```  
  
      COleServerItem* GetNextServerItem(  
   POSITION& pos   
) const;  
```  
  
#### Parameters  
 `pos`  
 A reference to a **POSITION** value set by a previous call to `GetNextServerItem`; the initial value is returned by the `GetStartPosition` member function.  
  
## Return Value  
 A pointer to the next server item in the document, or **NULL** if there are no more server items.  
  
## Remarks  
 After each call, the value of `pos` is set for the next item in the document, which might or might not be a server item.  
  
## Example  
 [!CODE [NVC_MFCOleServer#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleServer#2)]  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [COleDocument::GetStartPosition](../vs140/COleDocument--GetStartPosition.md)   
 [COleDocument::GetNextClientItem](../vs140/COleDocument--GetNextClientItem.md)   
 [COleDocument::GetNextItem](../vs140/COleDocument--GetNextItem.md)