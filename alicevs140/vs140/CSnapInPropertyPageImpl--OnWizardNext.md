---
title: "CSnapInPropertyPageImpl::OnWizardNext"
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
ms.assetid: 03f88118-1951-444d-8917-b4e21c7941a9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInPropertyPageImpl::OnWizardNext
This member function is called when the user clicks the `Next` button in a wizard.  
  
## Syntax  
  
```  
  
BOOL OnWizardNext( );  
  
```  
  
## Return Value  
  
-   0 to automatically advance to the next page.  
  
-   –1 to prevent the page from changing.  
  
 To jump to a page other than the next one, return the identifier of the dialog box to be displayed.  
  
## Remarks  
 Override this member function to specify some action the user must take when the `Next` button is clicked.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInPropertyPageImpl Class](../vs140/CSnapInPropertyPageImpl-Class.md)