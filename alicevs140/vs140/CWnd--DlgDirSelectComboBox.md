---
title: "CWnd::DlgDirSelectComboBox"
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
ms.assetid: 7a422a19-88eb-4d8d-87af-ba5eb58ca77b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::DlgDirSelectComboBox
Retrieves the current selection from the list box of a combo box.  
  
## Syntax  
  
```  
  
      BOOL DlgDirSelectComboBox(  
   LPTSTR lpString,  
   int nIDComboBox   
);  
```  
  
#### Parameters  
 `lpString`  
 Points to a buffer that is to receive the selected path.  
  
 `nIDComboBox`  
 Specifies the integer ID of the combo box in the dialog box.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 It assumes that the list box has been filled by the [DlgDirListComboBox](../vs140/CWnd--DlgDirListComboBox.md) member function and that the selection is a drive letter, a file, or a directory name.  
  
 The `DlgDirSelectComboBox` member function copies the selection to the specified buffer. If there is no selection, the contents of the buffer are not changed.  
  
 `DlgDirSelectComboBox` sends [CB_GETCURSEL](http://msdn.microsoft.com/library/windows/desktop/bb775845) and [CB_GETLBTEXT](http://msdn.microsoft.com/library/windows/desktop/bb775862) messages to the combo box.  
  
 It does not allow more than one filename to be returned from a combo box.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DlgDirListComboBox](../vs140/CWnd--DlgDirListComboBox.md)   
 [DlgDirSelectComboBoxEx](http://msdn.microsoft.com/library/windows/desktop/bb775937)