---
title: "CMFCToolBarsCustomizeDialog::EnableUserDefinedToolbars"
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
ms.assetid: d047265c-c8b5-4795-9e46-587781b455ba
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::EnableUserDefinedToolbars
Enables or disables creating new toolbars by using the **Customize** dialog box.  
  
## Syntax  
  
```  
void EnableUserDefinedToolbars(  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to enable the user-defined toolbars; `FALSE` to disable the toolbars.  
  
## Remarks  
 If `bEnable` is `TRUE`, the **New**, **Rename** and **Delete** buttons are displayed on the **Toolbars** page.  
  
 By default, or if `bEnable` is `FALSE`, these buttons are not displayed and the user cannot define new toolbars.  
  
## Requirements  
 **Header:** afxToolBarsCustomizeDialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)