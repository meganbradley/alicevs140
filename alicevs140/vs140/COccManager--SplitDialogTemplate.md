---
title: "COccManager::SplitDialogTemplate"
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
ms.assetid: 9b904622-d64f-44d2-a73e-babcdb84b42c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COccManager::SplitDialogTemplate
Called by the framework to split the ActiveX controls from common dialog controls.  
  
## Syntax  
  
```  
  
      virtual DLGTEMPLATE* SplitDialogTemplate(  
   const DLGTEMPLATE* pTemplate,  
   DLGITEMTEMPLATE** ppOleDlgItems   
);  
```  
  
#### Parameters  
 `pTemplate`  
 A pointer to the dialog template to be examined.  
  
 `ppOleDlgItems`  
 A list of pointers to dialog box items that are ActiveX controls.  
  
## Return Value  
 A pointer to a dialog template structure containing only non-ActiveX controls. If no ActiveX controls are present, **NULL** is returned.  
  
## Remarks  
 If any ActiveX controls are found, the template is analyzed and a new template, containing only non-ActiveX controls, is created. Any ActiveX controls found during this process are added to `ppOleDlgItems`.  
  
 If there are no ActiveX controls in the template, **NULL** is returned*.*  
  
> [!NOTE]
>  Memory allocated for the new template is freed in the `PostCreateDialog` function.  
  
 Override this function to customize this process.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COccManager Class](../vs140/COccManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COccManager::PostCreateDialog](../vs140/COccManager--PostCreateDialog.md)   
 [COccManager::PreCreateDialog](../vs140/COccManager--PreCreateDialog.md)