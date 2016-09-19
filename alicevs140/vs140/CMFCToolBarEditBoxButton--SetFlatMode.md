---
title: "CMFCToolBarEditBoxButton::SetFlatMode"
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
ms.assetid: fe048362-5d78-4525-aae5-05cb29033fe7
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::SetFlatMode
Specifies the flat style appearance of edit box buttons in the application.  
  
## Syntax  
  
```  
static void __stdcall SetFlatMode(  
   BOOL bFlat = TRUE  
);  
```  
  
#### Parameters  
 [in] `bFlat`  
 The flat style for edit box buttons. If this parameter is `TRUE`, the flat style appearance is enabled; otherwise the flat style appearance is disabled.  
  
## Remarks  
 The default flat style for edit box buttons is `TRUE`. Use the [CMFCToolBarEditBoxButton::IsFlatMode](../vs140/CMFCToolBarEditBoxButton--IsFlatMode.md) method to retrieve the flat style appearance for your application.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarEditBoxButton::IsFlatMode](../vs140/CMFCToolBarEditBoxButton--IsFlatMode.md)