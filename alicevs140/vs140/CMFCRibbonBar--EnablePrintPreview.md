---
title: "CMFCRibbonBar::EnablePrintPreview"
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
ms.assetid: 21ed94b0-a2c7-42a1-985f-0b327ca41c15
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::EnablePrintPreview
Enables or disables the **Print Preview** feature.  
  
## Syntax  
  
```  
void EnablePrintPreview(  
   BOOL bEnable = TRUE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to enable the **Print Preview** feature; `FALSE` to disable the **Print Preview** feature.  
  
## Remarks  
 If `bEnable` is `FALSE` and a print preview category exists, it is deleted.  
  
 By default the **Print Preview** feature is enabled.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)