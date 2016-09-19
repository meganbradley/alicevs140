---
title: "CMFCEditBrowseCtrl::EnableFileBrowseButton"
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
ms.assetid: fc8003d8-1347-47f9-ae39-48aed3ee5265
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCEditBrowseCtrl::EnableFileBrowseButton
Displays the browse button on the current edit browse control and puts the control in *file browse* mode.  
  
## Syntax  
  
```  
void EnableFileBrowseButton(  
   LPCTSTR lpszDefExt=NULL,  
   LPCTSTR lpszFilter=NULL,  
   DWORD dwFlags = OFN_HIDEREADONLY | OFN_OVERWRITEPROMPT  
);  
```  
  
#### Parameters  
 `lpszDefExt`  
 Specifies the default file name extension that is used in the file selection dialog box. The default value is `NULL`.  
  
 `lpszFilter`  
 Specifies the default filter string that is used in the file selection dialog box. The default value is `NULL`.  
  
 `dwFlags`  
 Dialog box flags. The default value is a bitwise combination (OR) of OFN_HIDEREADONLY and OFN_OVERWRITEPROMPT.  
  
## Remarks  
 When the edit browse control is in file browse mode and the user clicks the browse button, the control displays the standard file selection dialog box.  
  
 For a full list of available flags, see [OPENFILENAME structure](https://msdn.microsoft.com/library/ms646839.aspx).  
  
## Requirements  
 **Header:** afxeditbrowsectrl.h  
  
## See Also  
 [CMFCEditBrowseCtrl Class](../vs140/CMFCEditBrowseCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCEditBrowseCtrl::EnableBrowseButton](../vs140/CMFCEditBrowseCtrl--EnableBrowseButton.md)