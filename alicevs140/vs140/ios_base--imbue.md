---
title: "ios_base::imbue"
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
ms.assetid: 186d9bf2-abde-43a0-b571-8901941a819b
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::imbue
Changes the locale.  
  
## Syntax  
  
```  
  
      locale imbue(  
   const locale& _Loc  
);  
```  
  
#### Parameters  
 `_Loc`  
 The new locale setting.  
  
## Return Value  
 The previous locale.  
  
## Remarks  
 The member function stores `_Loc` in the locale object and then reports the callback event and `imbue_event`. It returns the previous stored value.  
  
## Example  
 See [basic_ios::imbue](../vs140/basic_ios--imbue.md) for a sample.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)