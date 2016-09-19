---
title: "CListBox::AddString"
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
ms.assetid: 263e95d9-40cd-41ba-94ef-045b76019df2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::AddString
Adds a string to a list box.  
  
## Syntax  
  
```  
  
      int AddString(  
   LPCTSTR lpszItem   
);  
```  
  
#### Parameters  
 `lpszItem`  
 Points to the null-terminated string that is to be added.  
  
## Return Value  
 The zero-based index to the string in the list box. The return value is **LB_ERR** if an error occurs; the return value is **LB_ERRSPACE** if insufficient space is available to store the new string.  
  
## Remarks  
 If the list box was not created with the [LBS_SORT](../vs140/List-Box-Styles.md) style, the string is added to the end of the list. Otherwise, the string is inserted into the list, and the list is sorted. If the list box was created with the **LBS_SORT** style but not the [LBS_HASSTRINGS](../vs140/List-Box-Styles.md) style, the framework sorts the list by one or more calls to the `CompareItem` member function.  
  
 Use [InsertString](../vs140/CListBox--InsertString.md) to insert a string into a specific location within the list box.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#3)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::InsertString](../vs140/CListBox--InsertString.md)   
 [CListBox::CompareItem](../vs140/CListBox--CompareItem.md)   
 [LB_ADDSTRING](http://msdn.microsoft.com/library/windows/desktop/bb775181)