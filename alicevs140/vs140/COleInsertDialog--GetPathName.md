---
title: "COleInsertDialog::GetPathName"
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
ms.assetid: 5a9d28e5-a434-4ce5-85f4-482bc1b22b90
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleInsertDialog::GetPathName
Call this function to get the full path of the selected file only if [DoModal](../vs140/COleInsertDialog--DoModal.md) returns **IDOK** and the selection type is not **COleInsertDialog::createNewItem**.  
  
## Syntax  
  
```  
  
CString GetPathName( ) const;    
```  
  
## Return Value  
 The full path to the file selected in the dialog box. If the selection type is `createNewItem`, this function returns a meaningless `CString` in release mode or causes an assertion in debug mode.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleInsertDialog Class](../vs140/COleInsertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleInsertDialog::GetSelectionType](../vs140/COleInsertDialog--GetSelectionType.md)   
 [COleInsertDialog::DoModal](../vs140/COleInsertDialog--DoModal.md)