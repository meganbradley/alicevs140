---
title: "CMFCToolBarEditBoxButton::SetStyle"
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
ms.assetid: 283e9be8-f10a-495d-9e6e-0b870d632c30
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::SetStyle
Specifies the style of a toolbar edit box control.  
  
## Syntax  
  
```  
virtual void SetStyle(  
   UINT nStyle   
);  
```  
  
#### Parameters  
 [in] `nStyle`  
 A new style to set.  
  
## Remarks  
 This method sets [CMFCToolBarButton::m_nStyle](../vs140/CMFCToolBarButton--m_nStyle.md) to `nStyle` It also disables the text box when the application is in Customize mode, and enables it when the application is not in Customize mode (see [CMFCToolBar::SetCustomizeMode](../vs140/CMFCToolBar--SetCustomizeMode.md) and [CMFCToolBar::IsCustomizeMode](../vs140/CMFCToolBar--IsCustomizeMode.md)). See [ToolBar Control Styles](../vs140/ToolBar-Control-Styles.md) for a list of valid style flags.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)