---
title: "CComboBox::GetCount"
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
ms.assetid: 6a624746-d346-438b-b53a-e54d390b6f16
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetCount
Call this member function to retrieve the number of items in the list-box portion of a combo box.  
  
## Syntax  
  
```  
  
int GetCount( ) const;  
```  
  
## Return Value  
 The number of items. The returned count is one greater than the index value of the last item (the index is zero-based). It is **CB_ERR** if an error occurs.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#14)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CB_GETCOUNT](http://msdn.microsoft.com/library/windows/desktop/bb775841)