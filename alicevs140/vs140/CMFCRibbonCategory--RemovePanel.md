---
title: "CMFCRibbonCategory::RemovePanel"
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
ms.assetid: e3950661-a087-4543-9dcd-e0f4bd2097cf
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::RemovePanel
Removes a ribbon panel from the ribbon category.  
  
## Syntax  
  
```cpp  
BOOL RemovePanel(  
   int nIndex,  
   BOOL bDelete = TRUE  
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 The index number of the panel to remove. Obtained by calling the [GetPanelIndex()](../vs140/CMFCRibbonCategory--GetPanelIndex.md) method.  
  
 [in] `bDelete`  
 `TRUE` to delete the panel object from memory; `FALSE` to remove the panel object without deleting it.  
  
## Return Value  
 `TRUE` if the method was successful; otherwise, `FALSE`.  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart](assetId:///07acbf55-d629-4dab-af20-8be36d71ac4b)