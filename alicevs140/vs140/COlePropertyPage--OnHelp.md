---
title: "COlePropertyPage::OnHelp"
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
ms.assetid: e6621dd1-5553-446f-a8b9-60822a52326e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::OnHelp
The framework calls this function when the user requests online help.  
  
## Syntax  
  
```  
  
      virtual BOOL OnHelp(  
   LPCTSTR lpszHelpDir   
);  
```  
  
#### Parameters  
 *lpszHelpDir*  
 Directory containing the property page's help file.  
  
## Return Value  
 The default implementation returns **FALSE**.  
  
## Remarks  
 Override it if your property page must perform any special action when the user accesses help. The default implementation does nothing and returns **FALSE**, which instructs the framework to call WinHelp.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)