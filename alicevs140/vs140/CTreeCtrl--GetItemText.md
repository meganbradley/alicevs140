---
title: "CTreeCtrl::GetItemText"
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
ms.assetid: 0403cb14-c4ea-4ffb-9613-9f872e334c89
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetItemText
Returns the text of the item specified by `hItem`.  
  
## Syntax  
  
```  
  
      CString GetItemText(  
   HTREEITEM hItem   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of the item whose text is to be retrieved.  
  
## Return Value  
 A `CString` object containing the item's text.  
  
## Example  
 See the example for [CTreeCtrl::GetNextItem](../vs140/CTreeCtrl--GetNextItem.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetItemText](../vs140/CTreeCtrl--SetItemText.md)