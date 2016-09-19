---
title: "CMFCToolBarEditBoxButton::OnGlobalFontsChanged"
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
ms.assetid: e2cc8dca-7213-4e02-a997-c711f481bf8c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::OnGlobalFontsChanged
Called by the framework when the global font has changed.  
  
## Syntax  
  
```  
virtual void OnGlobalFontsChanged();  
```  
  
## Remarks  
 This method extends the base class implementation ([CMFCToolBarButton::OnGlobalFontsChanged](../vs140/CMFCToolBarButton--OnGlobalFontsChanged.md)) by changing the font of the control to that of the global font.  
  
 For more information about global options that are available to your application, see [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md).  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnGlobalFontsChanged](../vs140/CMFCToolBarButton--OnGlobalFontsChanged.md)   
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)