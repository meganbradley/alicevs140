---
title: "CMFCToolBarButton::OnGlobalFontsChanged"
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
ms.assetid: 4185d0c6-e600-48e9-9f4a-9890cee5417b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::OnGlobalFontsChanged
Called by the framework when the global font has changed.  
  
## Syntax  
  
```  
virtual void OnGlobalFontsChanged();  
```  
  
## Remarks  
 The default implementation of this method does nothing. Override this method to update the font that is used to display the button text.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)