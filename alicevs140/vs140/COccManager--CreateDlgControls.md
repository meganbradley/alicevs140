---
title: "COccManager::CreateDlgControls"
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
ms.assetid: 6db96849-93ab-440a-9135-6f84ff2617d8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COccManager::CreateDlgControls
Call this function to create ActiveX controls specified by the `pOccDialogInfo` parameter.  
  
## Syntax  
  
```  
  
      virtual BOOL CreateDlgControls(  
   CWnd* pWndParent,  
   LPCTSTR lpszResourceName,  
   _AFX_OCC_DIALOG_INFO* pOccDialogInfo   
);  
virtual BOOL CreateDlgControls(  
   CWnd* pWndParent,  
   void* lpResource,  
   _AFX_OCC_DIALOG_INFO* pOccDialogInfo   
);  
```  
  
#### Parameters  
 *pWndParent*  
 A pointer to the parent of the dialog object.  
  
 `lpszResourceName`  
 The name of the resource being created.  
  
 `pOccDialogInfo`  
 A pointer to the dialog template used to create the dialog object.  
  
 `lpResource`  
 A pointer to a resource.  
  
## Return Value  
 Nonzero if the control was created successfully; otherwise zero.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COccManager Class](../vs140/COccManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)