---
title: "COccManager::PostCreateDialog"
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
ms.assetid: 6751215e-c37c-4492-8841-71e2c171d0a7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COccManager::PostCreateDialog
Called by the framework to free memory allocated for the dialog template.  
  
## Syntax  
  
```  
  
      virtual void PostCreateDialog(  
   _AFX_OCC_DIALOG_INFO* pOccDialogInfo   
);  
```  
  
#### Parameters  
 `pOccDialogInfo`  
 An **_AFX_OCC_DIALOG_INFO** structure containing information on the dialog template and any ActiveX controls hosted by the dialog.  
  
## Remarks  
 This memory was allocated by a call to `SplitDialogTemplate`, and was used for any hosted ActiveX controls in the dialog box.  
  
 Override this function to customize the process of cleaning up any resources used by the dialog box object.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COccManager Class](../vs140/COccManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COccManager::SplitDialogTemplate](../vs140/COccManager--SplitDialogTemplate.md)   
 [COccManager::PreCreateDialog](../vs140/COccManager--PreCreateDialog.md)