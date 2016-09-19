---
title: "CToolBarCtrl::AddString"
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
ms.assetid: 15920ba7-3af3-44a1-8402-617e8b4abf6c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::AddString
Adds a new string, passed as a resource ID, to the toolbar's internal list of strings.  
  
## Syntax  
  
```  
  
      int AddString(  
   UINT nStringID   
);  
```  
  
#### Parameters  
 *nStringID*  
 Resource identifier of the string resource to add to the toolbar control's string list.  
  
## Return Value  
 The zero-based index of the first new string added if successful; otherwise –1.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::AddStrings](../vs140/CToolBarCtrl--AddStrings.md)   
 [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md)   
 [CToolBarCtrl::InsertButton](../vs140/CToolBarCtrl--InsertButton.md)   
 [CToolBarCtrl::AddBitmap](../vs140/CToolBarCtrl--AddBitmap.md)