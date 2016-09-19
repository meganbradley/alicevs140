---
title: "CToolBarCtrl::AddStrings"
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
ms.assetid: c23992a2-8fdf-4a5f-8b86-2bed94b3cd68
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::AddStrings
Adds a new string or strings to the list of strings available for a toolbar control.  
  
## Syntax  
  
```  
  
      int AddStrings(  
   LPCTSTR lpszStrings   
);  
```  
  
#### Parameters  
 *lpszStrings*  
 Address of a buffer that contains one or more null-terminated strings to add to the toolbar's string list. The last string must be terminated with two null characters.  
  
## Return Value  
 The zero-based index of the first new string added if successful; otherwise –1.  
  
## Remarks  
 Strings in the buffer must be separated by a null character. You must ensure that the last string has two null terminators. To properly format a constant string, you might write it as:  
  
 [!CODE [NVC_MFCControlLadenDialog#72](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#72)]  
  
 or:  
  
 [!CODE [NVC_MFCControlLadenDialog#73](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#73)]  
  
 You should not pass a `CString` object to this function since it is not possible to have more than one null character in a `CString`.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::AddString](../vs140/CToolBarCtrl--AddString.md)   
 [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md)   
 [CToolBarCtrl::InsertButton](../vs140/CToolBarCtrl--InsertButton.md)   
 [CToolBarCtrl::AddBitmap](../vs140/CToolBarCtrl--AddBitmap.md)