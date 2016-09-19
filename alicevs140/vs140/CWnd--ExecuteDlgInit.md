---
title: "CWnd::ExecuteDlgInit"
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
ms.assetid: fa400931-7671-4c58-ba23-54e4be3a8f86
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ExecuteDlgInit
Initiates a dialog resource.  
  
## Syntax  
  
```  
  
      BOOL ExecuteDlgInit(  
   LPCTSTR lpszResourceName   
);  
BOOL ExecuteDlgInit(  
   LPVOID lpResource   
);  
```  
  
#### Parameters  
 `lpszResourceName`  
 A pointer to a null-terminated string specifying the name of the resource.  
  
 `lpResource`  
 A pointer to a resource.  
  
## Return Value  
 **TRUE** if a dialog resource is executed; otherwise **FALSE**.  
  
## Remarks  
 `ExecuteDlgInit` will use resources bound to the executing module, or resources from other sources. To accomplish this, `ExecuteDlgInit` finds a resource handle by calling `AfxFindResourceHandle`. If your MFC application does not use the shared DLL (MFCx0[U][D].DLL), **AfxFindResourceHandle** calls [AfxGetResourceHandle](../vs140/AfxGetResourceHandle.md), which returns the current resource handle for the executable. If your MFC application that uses MFCx0[U][D].DLL, `AfxFindResourceHandle` traverses the **CDynLinkLibrary** object list of shared and extension DLLs looking for the correct resource handle.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::OnInitDialog](../vs140/CDialog--OnInitDialog.md)   
 [WM_INITDIALOG](http://msdn.microsoft.com/library/windows/desktop/ms645428)