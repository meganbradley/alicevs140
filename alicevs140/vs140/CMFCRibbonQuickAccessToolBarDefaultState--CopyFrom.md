---
title: "CMFCRibbonQuickAccessToolBarDefaultState::CopyFrom"
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
ms.assetid: f3baf6a2-04a2-4965-ae4f-d6dca5330e7a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonQuickAccessToolBarDefaultState::CopyFrom
Copies the properties of one Quick Access Toolbar to another.  
  
## Syntax  
  
```  
void CopyFrom(  
   const CMFCRibbonQuickAccessToolBarDefaultState& src  
);  
```  
  
#### Parameters  
 [in] `src`  
 A reference to the source `CMFCRibbonQuickAccessToolBarDefaultState` object to copy from.  
  
## Remarks  
 This method copies each command from the source `CMFCRibbonQuickAccessToolBarDefaultState` object to this object by using the [CMFCRibbonQuickAccessToolBarDefaultState::AddCommand](../vs140/CMFCRibbonQuickAccessToolBarDefaultState--AddCommand.md) method.  
  
## Requirements  
 **Header:** afxribbonquickaccesstoolbar.h  
  
## See Also  
 [CMFCRibbonQuickAccessToolBarDefaultState Class](../vs140/CMFCRibbonQuickAccessToolBarDefaultState-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonQuickAccessToolBarDefaultState::AddCommand](../vs140/CMFCRibbonQuickAccessToolBarDefaultState--AddCommand.md)