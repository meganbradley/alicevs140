---
title: "CPictureHolder::GetDisplayString"
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
ms.assetid: b9146b2b-d236-4ef4-ba5c-794ae84fa234
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPictureHolder::GetDisplayString
Retrieves the string that is displayed in a container's property browser.  
  
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
 **Header:** afxwin.h  
  
## See Also  
 [CPictureHolder Class](../vs140/CPictureHolder-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)