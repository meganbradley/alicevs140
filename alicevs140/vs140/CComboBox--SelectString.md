---
title: "CComboBox::SelectString"
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
ms.assetid: 6170c6f5-0317-4e5a-ae2a-2a3b4907a857
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::SelectString
Searches for a string in the list box of a combo box, and if the string is found, selects the string in the list box and copies it to the edit control.  
  
## Syntax  
  
```  
  
      int SelectString(  
   int nStartAfter,  
   LPCTSTR lpszString   
);  
```  
  
#### Parameters  
 `nStartAfter`  
 Contains the zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by `nStartAfter`. If –1, the entire list box is searched from the beginning.  
  
 `lpszString`  
 Points to the null-terminated string that contains the prefix to search for. The search is case independent, so this string can contain any combination of uppercase and lowercase letters.  
  
## Return Value  
 The zero-based index of the selected item if the string was found. If the search was unsuccessful, the return value is **CB_ERR** and the current selection is not changed.  
  
## Remarks  
 A string is selected only if its initial characters (from the starting point) match the characters in the prefix string.  
  
 Note that the `SelectString` and `FindString` member functions both find a string, but the `SelectString` member function also selects the string.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#32](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#32)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::FindString](../vs140/CComboBox--FindString.md)   
 [CB_SELECTSTRING](http://msdn.microsoft.com/library/windows/desktop/bb775895)