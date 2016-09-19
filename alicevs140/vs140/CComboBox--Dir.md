---
title: "CComboBox::Dir"
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
ms.assetid: dd9b13ff-c1b9-4411-977a-5bd4c4c76a16
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::Dir
Adds a list of filenames or drives to the list box of a combo box.  
  
## Syntax  
  
```  
  
      int Dir(  
   UINT attr,  
   LPCTSTR lpszWildCard   
);  
```  
  
#### Parameters  
 `attr`  
 Can be any combination of the `enum` values described in [CFile::GetStatus](../vs140/CFile--GetStatus.md) or any combination of the following values:  
  
-   **DDL_READWRITE** File can be read from or written to.  
  
-   **DDL_READONLY** File can be read from but not written to.  
  
-   **DDL_HIDDEN** File is hidden and does not appear in a directory listing.  
  
-   **DDL_SYSTEM** File is a system file.  
  
-   **DDL_DIRECTORY** The name specified by `lpszWildCard` specifies a directory.  
  
-   **DDL_ARCHIVE** File has been archived.  
  
-   **DDL_DRIVES** Include all drives that match the name specified by `lpszWildCard`.  
  
-   **DDL_EXCLUSIVE** Exclusive flag. If the exclusive flag is set, only files of the specified type are listed. Otherwise, files of the specified type are listed in addition to "normal" files.  
  
 `lpszWildCard`  
 Points to a file-specification string. The string can contain wildcards (for example, *.\*).  
  
## Return Value  
 If the return value is greater than or equal to 0, it is the zero-based index of the last filename added to the list. The return value is **CB_ERR** if an error occurs; the return value is **CB_ERRSPACE** if insufficient space is available to store the new strings.  
  
## Remarks  
 This function is not supported by the Windows **ComboBoxEx** control. For more information on this control, see [ComboBoxEx Controls](http://msdn.microsoft.com/library/windows/desktop/bb775738) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#10)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DlgDirList](../vs140/CWnd--DlgDirList.md)   
 [CB_DIR](http://msdn.microsoft.com/library/windows/desktop/bb775832)   
 [CFile::GetStatus](../vs140/CFile--GetStatus.md)