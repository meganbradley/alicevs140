---
title: "CListBox::GetCount"
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
ms.assetid: a18bb8da-e8f1-4c28-84b5-ff5d68f401a9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetCount
Retrieves the number of items in a list box.  
  
## Syntax  
  
```  
  
int GetCount( ) const;  
```  
  
## Return Value  
 The number of items in the list box, or **LB_ERR** if an error occurs.  
  
## Remarks  
 The returned count is one greater than the index value of the last item (the index is zero-based).  
  
## Example  
 [!CODE [NVC_MFC_CListBox#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#12)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LB_GETCOUNT](http://msdn.microsoft.com/library/windows/desktop/bb775195)