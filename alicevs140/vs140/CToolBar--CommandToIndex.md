---
title: "CToolBar::CommandToIndex"
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
ms.assetid: 5eedd98f-0431-41f6-ab0f-3606a4c8fc8c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::CommandToIndex
This member function returns the index of the first toolbar button, starting at position 0, whose command ID matches `nIDFind`.  
  
## Syntax  
  
```  
  
      int CommandToIndex(  
   UINT nIDFind   
) const;  
```  
  
#### Parameters  
 `nIDFind`  
 Command ID of a toolbar button.  
  
## Return Value  
 The index of the button, or –1 if no button has the given command ID.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::GetItemID](../vs140/CToolBar--GetItemID.md)