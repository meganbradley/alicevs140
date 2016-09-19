---
title: "CMFCToolBar::ReplaceButton"
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
ms.assetid: 830335e8-88fb-4800-913a-8b24a05a4380
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::ReplaceButton
Replaces a toolbar button with another toolbar button.  
  
## Syntax  
  
```  
int ReplaceButton(  
   UINT uiCmd,  
   const CMFCToolBarButton& button,  
   BOOL bAll=FALSE   
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The command ID of the button to replace.  
  
 [in] `button`  
 A reference to the `CMFCToolBarButton` to insert.  
  
 [in] `bAll`  
 A Boolean value that specifies whether to replace all buttons that have the command ID specified by `uiCmd`. If this parameter is `TRUE`, all buttons that have the specified command ID are replaced. Otherwise, the first button is replaced.  
  
## Return Value  
 The number of buttons that are replaced. This method returns 0 if a button with the specified command ID does not exist on the toolbar.  
  
## Remarks  
 Call this method when you want to add toolbar buttons that cannot be loaded from resources. You can create a placeholder button at design-time and replace that button with a custom button when you initialize the toolbar. See the VisualStudioDemo sample for an example that uses this method.  
  
## Example  
 The following example demonstrates how to use the `ReplaceButton` method in the `CMFCToolBar` class. This code snippet is part of the [IE Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_IEDemo#6](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_IEDemo#6)]  
[!CODE [NVC_MFC_IEDemo#10](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_IEDemo#10)]  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)