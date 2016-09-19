---
title: "COleControlContainer::FindItem"
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
ms.assetid: 3bb9e8ca-eb26-4109-9aa0-c86b248938df
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::FindItem
Finds the custom site that hosts the specified item.  
  
## Syntax  
  
```  
  
      virtual COleControlSite* FindItem(  
   UINT nID   
) const;  
```  
  
#### Parameters  
 `nID`  
 The identifier of the item to be found.  
  
## Return Value  
 A pointer to the custom site of the specified item.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)