---
title: "CWnd::CheckDlgButton"
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
ms.assetid: 9418c960-a7d7-47c0-9090-db4e9c2d92df
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::CheckDlgButton
Selects (places a check mark next to) or clears (removes a check mark from) a button, or it changes the state of a three-state button.  
  
## Syntax  
  
```  
  
      void CheckDlgButton(  
   int nIDButton,  
   UINT nCheck   
);  
```  
  
#### Parameters  
 `nIDButton`  
 Specifies the button to be modified.  
  
 `nCheck`  
 Specifies the action to take. If `nCheck` is nonzero, the `CheckDlgButton` member function places a check mark next to the button; if 0, the check mark is removed. For three-state buttons, if `nCheck` is 2, the button state is indeterminate.  
  
## Remarks  
 The `CheckDlgButton` function sends a [BM_SETCHECK](http://msdn.microsoft.com/library/windows/desktop/bb775989) message to the specified button.  
  
## Example  
 [!CODE [NVC_MFCWindowing#75](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#75)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::IsDlgButtonChecked](../vs140/CWnd--IsDlgButtonChecked.md)   
 [CButton::SetCheck](../vs140/CButton--SetCheck.md)   
 [CheckDlgButton](http://msdn.microsoft.com/library/windows/desktop/bb761875)