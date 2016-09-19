---
title: "CSnapInPropertyPageImpl::OnQueryCancel"
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
ms.assetid: c4e2b220-f018-4a13-bd92-15a345c6c7e2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInPropertyPageImpl::OnQueryCancel
This member function is called when the user clicks the **Cancel** button and before the cancel action has taken place.  
  
## Syntax  
  
```  
  
BOOL OnQueryCancel( );  
  
```  
  
## Return Value  
 Nonzero to allow the cancel operation; otherwise 0.  
  
## Remarks  
 Override this member function to specify an action the program takes when the user clicks the **Cancel** button.  
  
 The default implementation of `OnQueryCancel` returns **TRUE**.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInPropertyPageImpl Class](../vs140/CSnapInPropertyPageImpl-Class.md)