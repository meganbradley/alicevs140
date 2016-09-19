---
title: "CSnapInPropertyPageImpl::QuerySiblings"
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
ms.assetid: 969d3050-3681-467a-ac64-9ae6882a2f95
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInPropertyPageImpl::QuerySiblings
Call this member function to forward a message to each page in the property sheet.  
  
## Syntax  
  
```  
  
      LRESULT QuerySiblings(  
   WPARAM wParam,  
   LPARAM lParam   
);  
```  
  
#### Parameters  
 `wParam`  
 [in] Specifies additional message-dependent information.  
  
 `lParam`  
 [in] Specifies additional message-dependent information.  
  
## Return Value  
 Nonzero if the message should not be forwarded to the next property page; otherwise zero.  
  
## Remarks  
 If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInPropertyPageImpl Class](../vs140/CSnapInPropertyPageImpl-Class.md)