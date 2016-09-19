---
title: "COlePropertyPage::GetPageSite"
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
ms.assetid: bf5ab37b-22a2-4f33-8dec-55393791a9b6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::GetPageSite
Gets a pointer to the property page's `IPropertyPageSite` interface.  
  
## Syntax  
  
```  
  
LPPROPERTYPAGESITE GetPageSite( );  
```  
  
## Return Value  
 A pointer to the property page's `IPropertyPageSite` interface.  
  
## Remarks  
 Controls and containers cooperate so that users can browse and edit control properties. The control provides property pages, each of which is an OLE object that allows the user to edit a related set of properties. The container provides a property frame that displays the property pages. For each page, the property frame provides a page site, which supports the `IPropertyPageSite` interface.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePropertyPage::OnSetPageSite](../vs140/COlePropertyPage--OnSetPageSite.md)