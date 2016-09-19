---
title: "COlePropertyPage::SetHelpInfo"
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
ms.assetid: c4b62d7a-3e4b-4205-9a7f-1087f2aa9c9c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::SetHelpInfo
Specifies tooltip information, the help filename, and the help context for your property page.  
  
## Syntax  
  
```  
  
      void SetHelpInfo(  
   LPCTSTR lpszDocString,  
   LPCTSTR lpszHelpFile = NULL,  
   DWORD dwHelpContext = 0   
);  
```  
  
#### Parameters  
 *lpszDocString*  
 A string containing brief help information for display in a status bar or other location.  
  
 `lpszHelpFile`  
 Name of the property page's help file.  
  
 *dwHelpContext*  
 Help context for the property page.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePropertyPage::OnHelp](../vs140/COlePropertyPage--OnHelp.md)