---
title: "CD2DTextLayout::SetLocaleName"
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
ms.assetid: d32220e7-9329-49b4-864f-05bdb8ef6377
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DTextLayout::SetLocaleName
Sets the locale name for text within a specified text range  
  
## Syntax  
  
```  
BOOL SetLocaleName(  
   LPCWSTR pwzLocaleName,  
   DWRITE_TEXT_RANGE textRange  
);  
```  
  
#### Parameters  
 `pwzLocaleName`  
 A null-terminated locale name string  
  
 `textRange`  
 Text range to which this change applies  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DTextLayout Class](../vs140/CD2DTextLayout-Class.md)