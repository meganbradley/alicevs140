---
title: "CWnd::GetCheckedRadioButton"
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
ms.assetid: 88202c09-51bd-4ad2-ba6b-31a475291631
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetCheckedRadioButton
Retrieves the ID of the currently checked radio button in the specified group.  
  
## Syntax  
  
```  
  
      int GetCheckedRadioButton(  
   int nIDFirstButton,  
   int nIDLastButton   
);  
```  
  
#### Parameters  
 `nIDFirstButton`  
 Specifies the integer identifier of the first radio button in the group.  
  
 `nIDLastButton`  
 Specifies the integer identifier of the last radio button in the group.  
  
## Return Value  
 ID of the checked radio button, or 0 if none is selected.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::CheckRadioButton](../vs140/CWnd--CheckRadioButton.md)