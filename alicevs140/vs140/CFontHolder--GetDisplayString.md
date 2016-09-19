---
title: "CFontHolder::GetDisplayString"
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
ms.assetid: f2b4d024-2d53-4fe7-9dc6-55a26b80d90e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontHolder::GetDisplayString
Retrieves a string that can be displayed in a container's property browser.  
  
## Syntax  
  
```  
  
      BOOL GetDisplayString(  
   CString& strValue   
);  
```  
  
#### Parameters  
 `strValue`  
 Reference to the [CString](../vs140/CStringT-Class.md) that is to hold the display string.  
  
## Return Value  
 Nonzero if the string is successfully retrieved; otherwise 0.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CFontHolder Class](../vs140/CFontHolder-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)