---
title: "CStatusBar::SetPaneText"
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
ms.assetid: 55337683-8804-4ff9-849e-e4c336d264b1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBar::SetPaneText
Call this member function to set the pane text to the string pointed to by `lpszNewText`.  
  
## Syntax  
  
```  
  
      BOOL SetPaneText(  
   int nIndex,  
   LPCTSTR lpszNewText,  
   BOOL bUpdate = TRUE   
);  
```  
  
#### Parameters  
 `nIndex`  
 Index of the pane whose text is to be set.  
  
 `lpszNewText`  
 Pointer to the new pane text.  
  
 *bUpdate*  
 If **TRUE**, the pane is invalidated after the text is set.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 After you call `SetPaneText`, you must add a UI update handler to display the new text in the status bar.  
  
## Example  
 [!CODE [NVC_MFCDocView#176](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#176)]  
  
 [!CODE [NVC_MFCDocView#177](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#177)]  
  
 [!CODE [NVC_MFCDocView#178](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#178)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBar::GetPaneText](../vs140/CStatusBar--GetPaneText.md)