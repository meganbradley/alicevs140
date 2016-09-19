---
title: "CDC::operator HDC"
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
ms.assetid: 583e82ec-8adb-4fe3-9cdb-e82cd5b1bdcf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::operator HDC
Use this operator to retrieve the device context handle of the `CDC` object.  
  
## Syntax  
  
```  
  
operator HDC( ) const;  
  
```  
  
## Return Value  
 If successful, the handle of the device context object; otherwise, **NULL**.  
  
## Remarks  
 You can use the handle to call Windows APIs directly.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)