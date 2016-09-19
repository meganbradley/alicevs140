---
title: "CFileDialog::GetNextPathName"
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
ms.assetid: 020a54b6-9425-409e-a17b-6e37bf564277
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetNextPathName
Call this function to retrieve the next filename from the group selected in the dialog box.  
  
## Syntax  
  
```  
  
      CString GetNextPathName(  
   POSITION& pos   
) const;  
```  
  
#### Parameters  
 `pos`  
 A reference to a **POSITION** value returned by a previous `GetNextPathName` or `GetStartPosition` function call. **NULL** if the end of the list has been reached.  
  
## Return Value  
 The full path of the file.  
  
## Remarks  
 The path of the filename includes the file's title plus the entire directory path. For example, `GetNextPathName` will return "C:\FILES\TEXT.DAT" for the file C:\FILES\TEXT.DAT. You can use `GetNextPathName` in a forward iteration loop if you establish the initial position with a call to `GetStartPosition`.  
  
 If the selection consists of only one file, that file name will be returned.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::GetFileName](../vs140/CFileDialog--GetFileName.md)   
 [CFileDialog::GetStartPosition](../vs140/CFileDialog--GetStartPosition.md)