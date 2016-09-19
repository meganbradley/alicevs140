---
title: "Benefits of Character Set Portability"
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
ms.topic: article
ms.assetid: bd60b925-1498-4e4f-897b-4c8ce66edcf7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Benefits of Character Set Portability
You can benefit from using MFC and C run-time portability features even if you do not currently intend to internationalize your application:  
  
-   Coding portably makes your code base flexible. You can later move it easily to Unicode or MBCS.  
  
-   Using Unicode makes your applications for Windows 2000 more efficient. Because Windows 2000 uses Unicode, non-Unicode strings passed to and from the operating system must be translated, which incurs overhead.  
  
-   Using MBCS enables you to support international markets on Win32 platforms other than Windows 2000, such as Windows 95 or Windows 98.  
  
## See Also  
 [Unicode and MBCS](../vs140/Unicode-and-MBCS.md)   
 [Support for Unicode](../vs140/Support-for-Unicode.md)