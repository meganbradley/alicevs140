---
title: "CStatusBar::CommandToIndex"
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
ms.assetid: 0fb6c4af-3941-4abe-90fe-4be54a379751
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBar::CommandToIndex
Gets the indicator index for a given ID.  
  
## Syntax  
  
```  
  
      int CommandToIndex(  
   UINT nIDFind   
) const;  
```  
  
#### Parameters  
 `nIDFind`  
 String ID of the indicator whose index is to be retrieved.  
  
## Return Value  
 The index of the indicator if successful; –1 if not successful.  
  
## Remarks  
 The index of the first indicator is 0.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBar::GetItemID](../vs140/CStatusBar--GetItemID.md)