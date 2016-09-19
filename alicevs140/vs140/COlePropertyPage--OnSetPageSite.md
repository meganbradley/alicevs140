---
title: "COlePropertyPage::OnSetPageSite"
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
ms.assetid: 4f6a4dc6-b55c-46ee-bbb9-c09866e95ca0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::OnSetPageSite
The framework calls this function when the property frame provides the property page's page site.  
  
## Syntax  
  
```  
  
virtual void OnSetPageSite( );  
```  
  
## Remarks  
 The default implementation loads the page's caption and attempts to determine the page's size from the dialog resource. Override this function if your property page requires any further action; your override should call the base-class implementation.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePropertyPage::GetPageSite](../vs140/COlePropertyPage--GetPageSite.md)