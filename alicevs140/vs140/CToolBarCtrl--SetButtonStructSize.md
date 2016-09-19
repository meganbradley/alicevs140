---
title: "CToolBarCtrl::SetButtonStructSize"
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
ms.assetid: 67c46b29-3e9b-4a20-b0bd-4ea33049334b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetButtonStructSize
Specifies the size of the `TBBUTTON` structure.  
  
## Syntax  
  
```  
  
      void SetButtonStructSize(  
   int nSize   
);  
```  
  
#### Parameters  
 `nSize`  
 Size, in bytes, of the `TBBUTTON` structure.  
  
## Remarks  
 If you wanted to store extra data in the `TBBUTTON` structure, you could either derive a new structure from `TBBUTTON`, adding the members you needed, or create a new structure that contains a `TBBUTTON` structure as its first member. You would then call this function to tell the toolbar control the size of the new structure.  
  
 See [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md) for more information on the `TBBUTTON` structure.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::Create](../vs140/CToolBarCtrl--Create.md)   
 [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md)   
 [CToolBarCtrl::InsertButton](../vs140/CToolBarCtrl--InsertButton.md)   
 [CToolBarCtrl::GetButton](../vs140/CToolBarCtrl--GetButton.md)