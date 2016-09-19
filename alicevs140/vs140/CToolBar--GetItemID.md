---
title: "CToolBar::GetItemID"
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
ms.assetid: 1330b82f-9ea1-4978-a247-4d6e68c58dbb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::GetItemID
This member function returns the command ID of the button or separator specified by `nIndex`.  
  
## Syntax  
  
```  
  
      UINT GetItemID(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Index of the item whose ID is to be retrieved.  
  
## Return Value  
 The command ID of the button or separator specified by `nIndex`.  
  
## Remarks  
 Separators return **ID_SEPARATOR**.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::CommandToIndex](../vs140/CToolBar--CommandToIndex.md)   
 [CControlBar::GetCount](../vs140/CControlBar--GetCount.md)