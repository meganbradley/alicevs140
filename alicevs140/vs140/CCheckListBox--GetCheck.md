---
title: "CCheckListBox::GetCheck"
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
ms.assetid: dd019fbd-5856-4e50-a108-1710f53f1dab
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCheckListBox::GetCheck
Retrieves the state of the specified check box.  
  
## Syntax  
  
```  
int GetCheck(  
   int nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 Zero-based index of a check box that is contained in the list box.  
  
## Return Value  
 The state of the specified check box. The following table lists possible values.  
  
|Value|Description|  
|-----------|-----------------|  
|`BST_CHECKED`|The check box is checked.|  
|`BST_UNCHECKED`|The check box is not checked.|  
|`BST_INDETERMINATE`|The check box state is indeterminate.|  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCheckListBox Class](../vs140/CCheckListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCheckListBox::OnGetCheckPosition](../vs140/CCheckListBox--OnGetCheckPosition.md)   
 [CCheckListBox::SetCheck](../vs140/CCheckListBox--SetCheck.md)   
 [CCheckListBox::SetCheckStyle](../vs140/CCheckListBox--SetCheckStyle.md)   
 [CCheckListBox::GetCheckStyle](../vs140/CCheckListBox--GetCheckStyle.md)