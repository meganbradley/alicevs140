---
title: "CMFCToolBar::GetShowTooltips"
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
ms.assetid: b7076943-a74d-4885-9642-6b9c83e0e03d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetShowTooltips
Specifies whether tool tips are displayed for toolbar buttons.  
  
## Syntax  
  
```  
static BOOL GetShowTooltips();  
```  
  
## Return Value  
 `TRUE` if tool tips are shown for toolbar buttons; otherwise `FALSE`.  
  
## Remarks  
 By default tool tips are shown. You can change this static flag by calling [CMFCToolBar::SetShowTooltips](../vs140/CMFCToolBar--SetShowTooltips.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)