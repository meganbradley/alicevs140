---
title: "CMFCToolBarsCustomizeDialog::SetUserCategory"
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
ms.assetid: 307489e8-35c8-4942-ad1e-42b9a7c88522
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::SetUserCategory
Specifies which category in the list of categories on the **Commands** page is the user category. You must call this function before you call [CMFCToolBarsCustomizeDialog::Create](../vs140/CMFCToolBarsCustomizeDialog--Create.md).  
  
## Syntax  
  
```  
BOOL SetUserCategory(  
   LPCTSTR lpszCategory   
);  
```  
  
#### Parameters  
 [in] `lpszCategory`  
 The name of the category.  
  
## Return Value  
 `TRUE` if the method is successful; otherwise `FALSE`.  
  
## Remarks  
 The user category setting is not currently used by the framework.  
  
## Requirements  
 **Header:** afxToolBarsCustomizeDialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)