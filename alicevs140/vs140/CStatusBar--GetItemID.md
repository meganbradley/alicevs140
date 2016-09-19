---
title: "CStatusBar::GetItemID"
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
ms.assetid: 8487feeb-b987-43a1-aefd-fafd60db767d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBar::GetItemID
Returns the ID of the indicator specified by `nIndex`.  
  
## Syntax  
  
```  
  
      UINT GetItemID(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Index of the indicator whose ID is to be retrieved.  
  
## Return Value  
 The ID of the indicator specified by `nIndex`.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBar::CommandToIndex](../vs140/CStatusBar--CommandToIndex.md)