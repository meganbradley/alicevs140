---
title: "CListBox::GetText"
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
ms.assetid: 6b81780d-2e93-4dd4-835d-44a2e442bc93
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetText
Gets a string from a list box.  
  
## Syntax  
  
```  
  
      int GetText(  
   int nIndex,  
   LPTSTR lpszBuffer   
) const;  
void GetText(  
   int nIndex,  
   CString& rString   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the string to be retrieved.  
  
 `lpszBuffer`  
 Points to the buffer that receives the string. The buffer must have sufficient space for the string and a terminating null character. The size of the string can be determined ahead of time by calling the `GetTextLen` member function.  
  
 `rString`  
 A reference to a `CString` object.  
  
## Return Value  
 The length (in bytes) of the string, excluding the terminating null character. If `nIndex` does not specify a valid index, the return value is **LB_ERR**.  
  
## Remarks  
 The second form of this member function fills a `CString` object with the string text.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#21)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::GetTextLen](../vs140/CListBox--GetTextLen.md)   
 [LB_GETTEXT](http://msdn.microsoft.com/library/windows/desktop/bb761313)