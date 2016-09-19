---
title: "CSnapInPropertyPageImpl::OnWizardBack"
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
ms.assetid: 9cec4c7a-507c-4b98-96db-38562374826c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInPropertyPageImpl::OnWizardBack
This member function is called when the user clicks the **Back** button in a wizard.  
  
## Syntax  
  
```  
  
BOOL OnWizardBack( );  
  
```  
  
## Return Value  
  
-   0 to automatically advance to the previous page.  
  
-   –1 to prevent the page from changing.  
  
 To jump to a page other than the next one, return the identifier of the dialog box to be displayed.  
  
## Remarks  
 Override this member function to specify some action the user must take when the **Back** button is clicked.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInPropertyPageImpl Class](../vs140/CSnapInPropertyPageImpl-Class.md)