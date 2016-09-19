---
title: "CMFCToolBarsCustomizeDialog::PostNcDestroy"
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
ms.assetid: a44c64cc-048a-4791-8fef-70224eeadd12
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::PostNcDestroy
Called by the framework after the window has been destroyed.  
  
## Syntax  
  
```  
virtual void PostNcDestroy();  
```  
  
## Remarks  
 This method extends the base class implementation, `CPropertySheet::PostNcDestroy`, by restoring the application to the previous mode.  
  
 The [CMFCToolBarsCustomizeDialog::Create](../vs140/CMFCToolBarsCustomizeDialog--Create.md) method puts the application in a special mode that limits the user to customization tasks.  
  
## Requirements  
 **Header:** afxtoolbarscustomizedialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarsCustomizeDialog::Create](../vs140/CMFCToolBarsCustomizeDialog--Create.md)