---
title: "CHeaderCtrl::GetItem"
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
ms.assetid: 931dc9cc-a41f-484e-8130-724b570311a8
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::GetItem
Retrieves information about a header control item.  
  
## Syntax  
  
```  
  
      BOOL GetItem(  
   int nPos,  
   HDITEM* pHeaderItem   
) const;  
```  
  
#### Parameters  
 `nPos`  
 Specifies the zero-based index of the item to retrieve.  
  
 `pHeaderItem`  
 Pointer to an [HDITEM](http://msdn.microsoft.com/library/windows/desktop/bb775247) structure that receives the new item. This structure is used with the `InsertItem` and `SetItem` member functions. Any flags set in the **mask** element ensure that values in the corresponding elements are properly filled in upon return. If the **mask** element is set to zero, values in the other structure elements are meaningless.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#10)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::SetItem](../vs140/CHeaderCtrl--SetItem.md)