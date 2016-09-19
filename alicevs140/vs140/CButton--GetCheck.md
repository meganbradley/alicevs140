---
title: "CButton::GetCheck"
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
ms.assetid: c919d5e6-aeda-49ff-8694-ddaed22e6e54
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetCheck
Retrieves the check state of a radio button or check box.  
  
## Syntax  
  
```  
  
int GetCheck( ) const;  
```  
  
## Return Value  
 The return value from a button control created with the **BS_AUTOCHECKBOX**, **BS_AUTORADIOBUTTON**, **BS_AUTO3STATE**, **BS_CHECKBOX**, **BS_RADIOBUTTON**, or **BS_3STATE** style is one of the following values:  
  
|Value|Meaning|  
|-----------|-------------|  
|**BST_UNCHECKED**|Button state is unchecked.|  
|**BST_CHECKED**|Button state is checked.|  
|**BST_INDETERMINATE**|Button state is indeterminate (applies only if the button has the **BS_3STATE** or **BS_AUTO3STATE** style).|  
  
 If the button has any other style, the return value is **BST_UNCHECKED**.  
  
## Example  
 [!CODE [NVC_MFC_CButton#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#6)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetState](../vs140/CButton--GetState.md)   
 [CButton::SetState](../vs140/CButton--SetState.md)   
 [CButton::SetCheck](../vs140/CButton--SetCheck.md)   
 [BM_GETCHECK](http://msdn.microsoft.com/library/windows/desktop/bb775986)