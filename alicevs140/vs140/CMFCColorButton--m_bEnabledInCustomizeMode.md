---
title: "CMFCColorButton::m_bEnabledInCustomizeMode"
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
ms.assetid: 6d621460-7278-4e6b-a974-9efb39a44d69
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorButton::m_bEnabledInCustomizeMode
Sets a color button to customization mode.  
  
## Syntax  
  
```  
BOOL m_bEnabledInCustomizeMode;  
```  
  
## Remarks  
 If you need to add a color button to a customization dialog's page (or allow the user to make another color selection during customization), enable the button by setting the `m_bEnabledInCustomizeMode` member to `TRUE`. By default, this member is set to `FALSE`.  
  
## Requirements  
 **Header:** afxcolorbutton.h  
  
## See Also  
 [CMFCColorButton Class](../vs140/CMFCColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)