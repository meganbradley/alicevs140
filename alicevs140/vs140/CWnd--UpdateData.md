---
title: "CWnd::UpdateData"
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
ms.assetid: 593893c2-7039-43fd-a165-f91329abd126
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::UpdateData
Call this member function to initialize data in a dialog box, or to retrieve and validate dialog data.  
  
## Syntax  
  
```  
  
      BOOL UpdateData(  
   BOOL bSaveAndValidate = TRUE   
);  
```  
  
#### Parameters  
 `bSaveAndValidate`  
 Flag that indicates whether dialog box is being initialized (**FALSE**) or data is being retrieved (**TRUE**).  
  
## Return Value  
 Nonzero if the operation is successful; otherwise 0. If *bSaveAndValidat*e is **TRUE**, then a return value of nonzero means that the data is successfully validated.  
  
## Remarks  
 The framework automatically calls `UpdateData` with `bSaveAndValidate` set to **FALSE** when a modal dialog box is created in the default implementation of [CDialog::OnInitDialog](../vs140/CDialog--OnInitDialog.md). The call occurs before the dialog box is visible. The default implementation of [CDialog::OnOK](../vs140/CDialog--OnOK.md) calls this member function with `bSaveAndValidate` set to **TRUE** to retrieve the data, and if successful, will close the dialog box. (If the Cancel button is clicked in the dialog box, the dialog box is closed without the data being retrieved.)  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DoDataExchange](../vs140/CWnd--DoDataExchange.md)