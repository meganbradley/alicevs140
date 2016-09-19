---
title: "COleInsertDialog::CreateItem"
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
ms.assetid: 61b12c70-bd17-465b-946f-edc1a2e88f76
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleInsertDialog::CreateItem
Call this function to create an object of type [COleClientItem](../vs140/COleClientItem-Class.md) only if [DoModal](../vs140/COleInsertDialog--DoModal.md) returns **IDOK**.  
  
## Syntax  
  
```  
  
      BOOL CreateItem(  
   COleClientItem* pItem   
);  
```  
  
#### Parameters  
 `pItem`  
 Points to the item to be created.  
  
## Return Value  
 Nonzero if item was created; otherwise 0.  
  
## Remarks  
 You must allocate the `COleClientItem` object before you can call this function.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleInsertDialog Class](../vs140/COleInsertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::CreateLinkFromFile](../vs140/COleClientItem--CreateLinkFromFile.md)   
 [COleClientItem::CreateFromFile](../vs140/COleClientItem--CreateFromFile.md)   
 [COleClientItem::CreateNewItem](../vs140/COleClientItem--CreateNewItem.md)   
 [COleClientItem::SetDrawAspect](../vs140/COleClientItem--SetDrawAspect.md)   
 [COleInsertDialog::GetSelectionType](../vs140/COleInsertDialog--GetSelectionType.md)   
 [COleInsertDialog::DoModal](../vs140/COleInsertDialog--DoModal.md)