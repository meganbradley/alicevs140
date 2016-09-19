---
title: "CMFCRibbonBar::GetQuickAccessCommands"
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
ms.assetid: eae081f8-c4bd-4b70-bef5-64e6ca79330d
caps.latest.revision: 20
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::GetQuickAccessCommands
Retrieves a list of command IDs for the ribbon elements on the quick access toolbar.  
  
## Syntax  
  
```  
void GetQuickAccessCommands(  
   CList<UINT,UINT>& lstCommands   
);  
```  
  
#### Parameters  
 [out] `lstCommands`  
 The list of command IDs for the ribbon elements on the quick access toolbar.  
  
## Remarks  
 The list does not contain ribbon elements that are control separators.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)