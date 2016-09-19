---
title: "CMFCShellListCtrl::GetCurrentFolderName"
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
ms.assetid: 936be4d2-c0b7-4b51-89b0-66f22555c0f6
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCShellListCtrl::GetCurrentFolderName
Retrieves the name of the currently selected folder in the [CMFCShellListCtrl](../vs140/CMFCShellListCtrl-Class.md) object.  
  
## Syntax  
  
```  
BOOL GetCurrentFolderName(  
   CString& strName   
) const;  
```  
  
#### Parameters  
 [out] `strName`  
 A reference to a string parameter where the method writes the name.  
  
## Return Value  
 Nonzero if successful; 0 otherwise.  
  
## Remarks  
 This method fails if there is no folder selected in the `CMFCShellListCtrl`.  
  
## Requirements  
 **Header:** afxshelllistctrl.h  
  
## See Also  
 [CMFCShellListCtrl Class](../vs140/CMFCShellListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)