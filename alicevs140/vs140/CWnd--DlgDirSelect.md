---
title: "CWnd::DlgDirSelect"
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
ms.assetid: a72d7b0d-74f9-41ef-a101-9709755a3b5f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::DlgDirSelect
Retrieves the current selection from a list box.  
  
## Syntax  
  
```  
  
      BOOL DlgDirSelect(  
   LPTSTR lpString,  
   int nIDListBox   
);  
```  
  
#### Parameters  
 `lpString`  
 Points to a buffer that is to receive the current selection in the list box.  
  
 `nIDListBox`  
 Specifies the integer ID of a list box in the dialog box.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 It assumes that the list box has been filled by the [DlgDirList](../vs140/CWnd--DlgDirList.md) member function and that the selection is a drive letter, a file, or a directory name.  
  
 The `DlgDirSelect` member function copies the selection to the buffer given by `lpString`. If there is no selection, `lpString` does not change.  
  
 `DlgDirSelect` sends [LB_GETCURSEL](http://msdn.microsoft.com/library/windows/desktop/bb775197) and [LB_GETTEXT](http://msdn.microsoft.com/library/windows/desktop/bb761313) messages to the list box.  
  
 It does not allow more than one filename to be returned from a list box. The list box must not be a multiple-selection list box.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DlgDirList](../vs140/CWnd--DlgDirList.md)   
 [CWnd::DlgDirListComboBox](../vs140/CWnd--DlgDirListComboBox.md)   
 [CWnd::DlgDirSelectComboBox](../vs140/CWnd--DlgDirSelectComboBox.md)   
 [DlgDirSelectEx](http://msdn.microsoft.com/library/windows/desktop/bb761368)