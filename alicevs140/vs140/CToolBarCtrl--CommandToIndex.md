---
title: "CToolBarCtrl::CommandToIndex"
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
ms.assetid: 26125f9f-0202-4cd3-a8f1-431e13ade83e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::CommandToIndex
Retrieves the zero-based index for the button associated with the specified command identifier.  
  
## Syntax  
  
```  
  
      UINT CommandToIndex(  
   UINT nID   
) const;  
```  
  
#### Parameters  
 `nID`  
 Command ID whose button index you want to find.  
  
## Return Value  
 The zero-based index for the button associated with the command ID.  
  
## Remarks  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrlOverview](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetCmdID](../vs140/CToolBarCtrl--SetCmdID.md)   
 [CToolBarCtrl::GetButton](../vs140/CToolBarCtrl--GetButton.md)   
 [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md)   
 [CToolBarCtrl::InsertButton](../vs140/CToolBarCtrl--InsertButton.md)