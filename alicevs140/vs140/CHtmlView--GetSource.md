---
title: "CHtmlView::GetSource"
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
ms.assetid: 555fdcc6-e428-409c-8e99-8d4cf50422e6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetSource
Call this member function to retrieve the HTML source code for the web page.  
  
## Syntax  
  
```  
  
      BOOL GetSource(  
   CString& strRef   
);  
```  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
#### Parameters  
 `refString`  
 A [CString](../vs140/CStringT-Class.md) that will hold the source code.  
  
## Remarks  
 This function is equivalent to the "View Source" command in Internet Explorer, except that the source code is returned in a `CString`.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)