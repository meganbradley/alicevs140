---
title: "CComboBox::FindString"
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
ms.assetid: 1568ca40-c990-4922-9bba-9532a6bc6610
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::FindString
Finds, but doesn't select, the first string that contains the specified prefix in the list box of a combo box.  
  
## Syntax  
  
```  
  
      int FindString(  
   int nStartAfter,  
   LPCTSTR lpszString   
) const;  
```  
  
#### Parameters  
 `nStartAfter`  
 Contains the zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by `nStartAfter`. If –1, the entire list box is searched from the beginning.  
  
 `lpszString`  
 Points to the null-terminated string that contains the prefix to search for. The search is case independent, so this string can contain any combination of uppercase and lowercase letters.  
  
## Return Value  
 If the return value is greater than or equal to 0, it is the zero-based index of the matching item. It is **CB_ERR** if the search was unsuccessful.  
  
## Remarks  
 This function is not supported by the Windows **ComboBoxEx** control. For more information on this control, see [ComboBoxEx Controls](http://msdn.microsoft.com/library/windows/desktop/bb775738) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#12)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::SelectString](../vs140/CComboBox--SelectString.md)   
 [CComboBox::SetCurSel](../vs140/CComboBox--SetCurSel.md)   
 [CB_FINDSTRING](http://msdn.microsoft.com/library/windows/desktop/bb775835)