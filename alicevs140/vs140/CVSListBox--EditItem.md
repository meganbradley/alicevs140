---
title: "CVSListBox::EditItem"
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
ms.assetid: 497b3271-e598-47a6-887b-74d1008cc735
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CVSListBox::EditItem
Starts an edit operation on the text of a list control item.  
  
## Syntax  
  
```  
virtual BOOL EditItem(  
   int iIndex   
);  
```  
  
#### Parameters  
 [in] `iIndex`  
 Zero-based index of a list control item.  
  
## Return Value  
 `TRUE` if the edit operation starts successfully; otherwise, `FALSE`.  
  
## Remarks  
 The user starts an edit operation either by double-clicking the label of an item, or by pressing the **F2** or **SPACEBAR** key when an item has the focus.  
  
## Requirements  
 **Header:** afxvslistbox.h  
  
## See Also  
 [CVSListBox Class](../vs140/CVSListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)