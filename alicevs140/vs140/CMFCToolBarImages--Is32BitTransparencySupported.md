---
title: "CMFCToolBarImages::Is32BitTransparencySupported"
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
ms.assetid: bdf71c8c-bbac-43eb-bea9-23f8247c9c2c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::Is32BitTransparencySupported
Specifies whether the operating system supports 32-bit alpha blending.  
  
## Syntax  
  
```  
static BOOL Is32BitTransparencySupported();  
```  
  
## Return Value  
 `TRUE` if 32-bit alpha blending is supported; otherwise `FALSE`.  
  
## Remarks  
 Use this static method to determine at runtime whether the operating system supports 32-bit alpha blending. This feature is supported on [!INCLUDE[win2kfamily](../vs140/includes/win2kfamily_md.md)] and later versions.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)