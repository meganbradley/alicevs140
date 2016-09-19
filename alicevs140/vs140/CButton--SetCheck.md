---
title: "CButton::SetCheck"
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
ms.assetid: 202d1f1f-b795-4df7-9339-18e27015024d
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetCheck
Sets or resets the check state of a radio button or check box.  
  
## Syntax  
  
```  
  
      void SetCheck(  
   int nCheck   
);  
```  
  
#### Parameters  
 `nCheck`  
 Specifies the check state. This parameter can be one of the following:  
  
|Value|Meaning|  
|-----------|-------------|  
|**BST_UNCHECKED**|Set the button state to unchecked.|  
|**BST_CHECKED**|Set the button state to checked.|  
|**BST_INDETERMINATE**|Set the button state to indeterminate. This value can be used only if the button has the **BS_3STATE** or **BS_AUTO3STATE** style.|  
  
## Remarks  
 This member function has no effect on a pushbutton.  
  
## Example  
 [!CODE [NVC_MFC_CButton#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#6)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetCheck](../vs140/CButton--GetCheck.md)   
 [CButton::GetState](../vs140/CButton--GetState.md)   
 [CButton::SetState](../vs140/CButton--SetState.md)   
 [BM_SETCHECK](http://msdn.microsoft.com/library/windows/desktop/bb775989)