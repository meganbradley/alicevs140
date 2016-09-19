---
title: "CToolBarCtrl::SetCmdID"
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
ms.assetid: 19ae520e-8084-4d5b-adc4-e6917dbcc90e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetCmdID
Sets the command identifier that will be sent to the owner window when the specified button is pressed.  
  
## Syntax  
  
```  
  
      BOOL SetCmdID(  
   int nIndex,  
   UINT nID   
);  
```  
  
#### Parameters  
 `nIndex`  
 The zero-based index of the button whose command ID is to be set.  
  
 `nID`  
 The command ID to set the selected button to.  
  
## Return Value  
 Returns nonzero if successful; otherwise zero.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::CommandToIndex](../vs140/CToolBarCtrl--CommandToIndex.md)   
 [CToolBarCtrl::GetButton](../vs140/CToolBarCtrl--GetButton.md)   
 [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md)   
 [CToolBarCtrl::InsertButton](../vs140/CToolBarCtrl--InsertButton.md)