---
title: "CComboBox::FindStringExact"
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
ms.assetid: fc6b7a72-e80d-45c5-9feb-3c0df342dbc5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::FindStringExact
Call the `FindStringExact` member function to find the first list-box string (in a combo box) that matches the string specified in `lpszFind`.  
  
## Syntax  
  
```  
  
      int FindStringExact(  
   int nIndexStart,  
   LPCTSTR lpszFind   
) const;  
```  
  
#### Parameters  
 `nIndexStart`  
 Specifies the zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by `nIndexStart`. If `nIndexStart` is –1, the entire list box is searched from the beginning.  
  
 `lpszFind`  
 Points to the null-terminated string to search for. This string can contain a complete filename, including the extension. The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.  
  
## Return Value  
 The zero-based index of the matching item, or **CB_ERR** if the search was unsuccessful.  
  
## Remarks  
 If the combo box was created with an owner-draw style but without the [CBS_HASSTRINGS](../vs140/Combo-Box-Styles.md) style, `FindStringExact` attempts to match the doubleword value against the value of `lpszFind`.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#13)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::FindString](../vs140/CComboBox--FindString.md)   
 [CB_FINDSTRINGEXACT](http://msdn.microsoft.com/library/windows/desktop/bb775837)