---
title: "COccManager::PreCreateDialog"
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
ms.assetid: 4e5cee6d-1cf9-4a5c-bbb6-a48ae2f45f50
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COccManager::PreCreateDialog
Called by the framework to process a dialog template for ActiveX controls before creating the actual dialog box.  
  
## Syntax  
  
```  
  
      virtual const DLGTEMPLATE* PreCreateDialog(  
   _AFX_OCC_DIALOG_INFO* pOccDialogInfo,  
   const DLGTEMPLATE* pOrigTemplate   
);  
```  
  
#### Parameters  
 `pOccDialogInfo`  
 An **_AFX_OCC_DIALOG_INFO** structure containing information on the dialog template and any ActiveX controls hosted by the dialog.  
  
 *pOrigTemplate*  
 A pointer to the dialog template to be used in creating the dialog box.  
  
## Return Value  
 A pointer to a dialog template structure used to create the dialog box.  
  
## Remarks  
 The default behavior makes a call to `SplitDialogTemplate`, determining if there are any ActiveX controls present and then returns the resultant dialog template.  
  
 Override this function to customize the process of creating a dialog box hosting ActiveX controls.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COccManager Class](../vs140/COccManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COccManager::SplitDialogTemplate](../vs140/COccManager--SplitDialogTemplate.md)   
 [COccManager::PostCreateDialog](../vs140/COccManager--PostCreateDialog.md)