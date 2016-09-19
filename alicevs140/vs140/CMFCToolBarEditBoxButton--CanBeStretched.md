---
title: "CMFCToolBarEditBoxButton::CanBeStretched"
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
ms.assetid: fb8d3df2-875e-46df-a017-438bc1bd3ce6
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::CanBeStretched
Specifies whether a user can stretch the button during customization.  
  
## Syntax  
  
```  
virtual BOOL CanBeStretched() const;  
```  
  
## Return Value  
 This method returns `TRUE`.  
  
## Remarks  
 By default, the framework does not allow the user to stretch a toolbar button during customization. This method extends the base class implementation ([CMFCToolBarButton::CanBeStretched](../vs140/CMFCToolBarButton--CanBeStretched.md)) by allowing the user to stretch an edit box toolbar button during customization.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::CanBeStretched](../vs140/CMFCToolBarButton--CanBeStretched.md)