---
title: "CSnapInPropertyPageImpl::OnWizardFinish"
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
ms.assetid: c36ce42c-7b4b-44a1-b932-6a5f7f267b6d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInPropertyPageImpl::OnWizardFinish
This member function is called when the user clicks the **Finish** button in a wizard.  
  
## Syntax  
  
```  
  
BOOL OnWizardFinish( );  
  
```  
  
## Return Value  
 Nonzero if the property sheet is destroyed when the wizard finishes; otherwise zero.  
  
## Remarks  
 Override this member function to specify some action the user must take when the **Finish** button is clicked.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInPropertyPageImpl Class](../vs140/CSnapInPropertyPageImpl-Class.md)