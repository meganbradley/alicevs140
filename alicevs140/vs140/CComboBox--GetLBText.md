---
title: "CComboBox::GetLBText"
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
ms.assetid: 63fe09d9-8df7-46eb-ae6a-f6c97bf6e750
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetLBText
Gets a string from the list box of a combo box.  
  
## Syntax  
  
```  
  
      int GetLBText(  
   int nIndex,  
   LPTSTR lpszText   
) const;  
void GetLBText(  
   int nIndex,  
   CString& rString   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Contains the zero-based index of the list-box string to be copied.  
  
 `lpszText`  
 Points to a buffer that is to receive the string. The buffer must have sufficient space for the string and a terminating null character.  
  
 `rString`  
 A reference to a `CString`.  
  
## Return Value  
 The length (in bytes) of the string, excluding the terminating null character. If `nIndex` does not specify a valid index, the return value is **CB_ERR**.  
  
## Remarks  
 The second form of this member function fills a `CString` object with the item's text.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#24](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#24)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetLBTextLen](../vs140/CComboBox--GetLBTextLen.md)   
 [CB_GETLBTEXT](http://msdn.microsoft.com/library/windows/desktop/bb775862)