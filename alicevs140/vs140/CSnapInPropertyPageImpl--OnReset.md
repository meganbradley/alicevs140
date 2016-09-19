---
title: "CSnapInPropertyPageImpl::OnReset"
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
ms.assetid: 67167d48-a21c-437a-ac29-cb9b77d80349
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInPropertyPageImpl::OnReset
This member function is called when the user clicks the **Cancel** button.  
  
## Syntax  
  
```  
  
void OnReset( );  
  
```  
  
## Remarks  
 When this function is called, changes to all property pages that were made by the user previously clicking the **Apply Now** button are discarded, and the property sheet retains focus.  
  
 Override this member function to specify what action the program takes when the user clicks the **Cancel** button.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInPropertyPageImpl Class](../vs140/CSnapInPropertyPageImpl-Class.md)