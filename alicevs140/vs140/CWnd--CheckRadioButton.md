---
title: "CWnd::CheckRadioButton"
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
ms.assetid: 5f82a5ed-f568-4322-a417-e36b2a589417
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::CheckRadioButton
Selects (adds a check mark to) a given radio button in a group and clears (removes a check mark from) all other radio buttons in the group.  
  
## Syntax  
  
```  
  
      void CheckRadioButton(  
   int nIDFirstButton,  
   int nIDLastButton,  
   int nIDCheckButton   
);  
```  
  
#### Parameters  
 `nIDFirstButton`  
 Specifies the integer identifier of the first radio button in the group.  
  
 `nIDLastButton`  
 Specifies the integer identifier of the last radio button in the group.  
  
 `nIDCheckButton`  
 Specifies the integer identifier of the radio button to be checked.  
  
## Remarks  
 The `CheckRadioButton` function sends a [BM_SETCHECK](http://msdn.microsoft.com/library/windows/desktop/bb775989) message to the specified radio button.  
  
## Example  
 [!CODE [NVC_MFCWindowing#76](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#76)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetCheckedRadioButton](../vs140/CWnd--GetCheckedRadioButton.md)   
 [CButton::SetCheck](../vs140/CButton--SetCheck.md)   
 [CheckRadioButton](http://msdn.microsoft.com/library/windows/desktop/bb761877)