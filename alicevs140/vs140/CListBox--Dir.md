---
title: "CListBox::Dir"
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
ms.assetid: b345bc4d-6b2a-45f2-a795-5b6380d6e860
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::Dir
Adds a list of filenames, drives, or both to a list box.  
  
## Syntax  
  
```  
  
      int Dir(  
   UINT attr,  
   LPCTSTR lpszWildCard   
);  
```  
  
#### Parameters  
 `attr`  
 Can be any combination of the `enum` values described in **CFile::GetStatu**[s](../vs140/CFile--GetStatus.md), or any combination of the following values:  
  
|Value|Meaning|  
|-----------|-------------|  
|0x0000|File can be read from or written to.|  
|0x0001|File can be read from but not written to.|  
|0x0002|File is hidden and does not appear in a directory listing.|  
|0x0004|File is a system file.|  
|0x0010|The name specified by `lpszWildCard` specifies a directory.|  
|0x0020|File has been archived.|  
|0x4000|Include all drives that match the name specified by `lpszWildCard`.|  
|0x8000|Exclusive flag. If the exclusive flag is set, only files of the specified type are listed. Otherwise, files of the specified type are listed in addition to "normal" files.|  
  
 `lpszWildCard`  
 Points to a file-specification string. The string can contain wildcards (for example, *.\*).  
  
## Return Value  
 The zero-based index of the last filename added to the list. The return value is **LB_ERR** if an error occurs; the return value is **LB_ERRSPACE** if insufficient space is available to store the new strings.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#8)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DlgDirList](../vs140/CWnd--DlgDirList.md)   
 [LB_DIR](http://msdn.microsoft.com/library/windows/desktop/bb775185)   
 [CFile::GetStatus](../vs140/CFile--GetStatus.md)