---
title: "CButton::GetState"
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
ms.assetid: f1a2c88f-1bd9-485d-88e6-df1803a038c6
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetState
Retrieves the state of a button control.  
  
## Syntax  
  
```  
  
UINT GetState( ) const;  
```  
  
## Return Value  
 A bit field that contains the combination of values that indicate the current state of a button control. The following table lists possible values.  
  
|Button State|Value|Description|  
|------------------|-----------|-----------------|  
|`BST_UNCHECKED`|0x0000|The initial state.|  
|`BST_CHECKED`|0x0001|The button control is checked.|  
|`BST_INDETERMINATE`|0x0002|The state is indeterminate (only possible when the button control has three states).|  
|`BST_PUSHED`|0x0004|The button control is pressed.|  
|`BST_FOCUS`|0x0008|The button control has the focus.|  
  
## Remarks  
 A button control with the `BS_3STATE` or `BS_AUTO3STATE` button style creates a check box that has a third state that is named the indeterminate state. The indeterminate state indicates that the check box is neither checked nor unchecked.  
  
## Example  
 [!CODE [NVC_MFC_CButton#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#9)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetCheck](../vs140/CButton--GetCheck.md)   
 [CButton::SetCheck](../vs140/CButton--SetCheck.md)   
 [CButton::SetState](../vs140/CButton--SetState.md)   
 [BM_GETSTATE](http://msdn.microsoft.com/library/windows/desktop/bb775988)