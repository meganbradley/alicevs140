---
title: "CMFCRibbonMiniToolBar::SetCommands"
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
ms.assetid: 8dd97c5b-2662-473b-89f1-fb62af1f7e1c
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonMiniToolBar::SetCommands
Sets the list of commands to be displayed on the toolbar.  
  
## Syntax  
  
```  
void SetCommands(  
    CMFCRibbonBar* pRibbonBar,  
    const CList<UINT,UINT>& lstCommands   
);  
```  
  
#### Parameters  
 [in] `pRibbonBar`  
 The ribbon bar that the mini toolbar searches for the buttons to display.  
  
 [in] `lstCommands`  
 The list of commands to be displayed on the mini toolbar. All ribbon categories are searched to find the associated buttons.  
  
## Remarks  
 Use this function to set the list of commands to be displayed in the mini toolbar.  
  
## Example  
 The following example demonstrates how to use the `SetCommands` method of the `CMFCRibbonMiniToolBar` class. This code snippet is part of the [MS Office 2007 Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_MSOffice2007Demo#9](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_MSOffice2007Demo#9)]  
  
## Requirements  
 **Header:** afxRibbonMiniToolBar.h  
  
## See Also  
 [CMFCRibbonMiniToolBar Class](../vs140/CMFCRibbonMiniToolBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)