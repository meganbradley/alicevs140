---
title: "CCheckListBox::OnGetCheckPosition"
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
ms.assetid: 457281ee-7213-472f-92b3-bd199e041527
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCheckListBox::OnGetCheckPosition
The framework calls this function to get the position and size of the check box in an item.  
  
## Syntax  
  
```  
  
      virtual CRect OnGetCheckPosition(  
   CRect rectItem,  
   CRect rectCheckBox   
);  
```  
  
#### Parameters  
 *rectItem*  
 The position and size of the list item.  
  
 `rectCheckBox`  
 The default position and size of an item's check box.  
  
## Return Value  
 The position and size of an item's check box.  
  
## Remarks  
 The default implementation only returns the default position and size of the check box (`rectCheckBox`). By default, a check box is aligned in the upper-left corner of an item and is the standard check box size. There may be cases where you want the check boxes on the right, or want a larger or smaller check box. In these cases, override `OnGetCheckPosition` to change the check box position and size within the item.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCheckListBox Class](../vs140/CCheckListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCheckListBox::SetCheck](../vs140/CCheckListBox--SetCheck.md)   
 [CCheckListBox::SetCheckStyle](../vs140/CCheckListBox--SetCheckStyle.md)   
 [CCheckListBox::GetCheck](../vs140/CCheckListBox--GetCheck.md)   
 [CCheckListBox::GetCheckStyle](../vs140/CCheckListBox--GetCheckStyle.md)