---
title: "CDC::GetSafeHdc"
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
ms.assetid: 7e845e30-2da1-4c70-a205-47ae10e76992
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetSafeHdc
Call this member function to get [m_hDC](../vs140/CDC--m_hDC.md), the output device context.  
  
## Syntax  
  
```  
  
HDC GetSafeHdc( ) const;  
```  
  
## Return Value  
 A device context handle.  
  
## Remarks  
 This member function also works with null pointers.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)