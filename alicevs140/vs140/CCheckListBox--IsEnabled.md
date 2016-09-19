---
title: "CCheckListBox::IsEnabled"
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
ms.assetid: de8b16f1-78ab-4f22-858e-9ca3126967eb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCheckListBox::IsEnabled
Call this function to determine whether an item is enabled.  
  
## Syntax  
  
```  
  
      BOOL IsEnabled(  
   int nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 Index of the item.  
  
## Return Value  
 Nonzero if the item is enabled; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCheckListBox Class](../vs140/CCheckListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCheckListBox::Enable](../vs140/CCheckListBox--Enable.md)