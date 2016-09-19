---
title: "COleClientItem::COleClientItem"
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
ms.assetid: 00886648-ccb5-4f20-9715-5b7271f7ef97
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::COleClientItem
Constructs a `COleClientItem` object and adds it to the container document's collection of document items, which constructs only the C++ object and does not perform any OLE initialization.  
  
## Syntax  
  
```  
  
      COleClientItem(  
   COleDocument* pContainerDoc = NULL   
);  
```  
  
#### Parameters  
 `pContainerDoc`  
 Pointer to the container document that will contain this item. This can be any [COleDocument](../vs140/COleDocument-Class.md) derivative.  
  
## Remarks  
 If you pass a **NULL** pointer, no addition is made to the container document. You must explicitly call [COleDocument::AddItem](../vs140/COleDocument--AddItem.md).  
  
 You must call one of the following creation member functions before you use the OLE item:  
  
-   [CreateFromClipboard](../vs140/COleClientItem--CreateFromClipboard.md)  
  
-   [CreateFromData](../vs140/COleClientItem--CreateFromData.md)  
  
-   [CreateFromFile](../vs140/COleClientItem--CreateFromFile.md)  
  
-   [CreateStaticFromClipboard](../vs140/COleClientItem--CreateStaticFromClipboard.md)  
  
-   [CreateStaticFromData](../vs140/COleClientItem--CreateStaticFromData.md)  
  
-   [CreateLinkFromClipboard](../vs140/COleClientItem--CreateLinkFromClipboard.md)  
  
-   [CreateLinkFromData](../vs140/COleClientItem--CreateLinkFromData.md)  
  
-   [CreateLinkFromFile](../vs140/COleClientItem--CreateLinkFromFile.md)  
  
-   [CreateNewItem](../vs140/COleClientItem--CreateNewItem.md)  
  
-   [CreateCloneFrom](../vs140/COleClientItem--CreateCloneFrom.md)  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [COleDocument::AddItem](../vs140/COleDocument--AddItem.md)