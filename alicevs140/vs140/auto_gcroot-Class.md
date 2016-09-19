---
title: "auto_gcroot Class"
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
ms.assetid: b5790912-265d-463e-a486-47302e91042a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_gcroot Class
Automatic resource management (like [std::auto_ptr](../vs140/auto_ptr-Class.md)) which can be used to embed a virtual handle into a native type.  
  
## Syntax  
  
```  
template<typename _element_type>  
class auto_gcroot;  
```  
  
#### Parameters  
 `_element_type`  
 The managed type to be embedded.  
  
## Requirements  
 **Header file** <msclr\auto_gcroot.h>  
  
 **Namespace** msclr  
  
## See Also  
 [<msclr\auto_gcroot.h> Header](../vs140/auto_gcroot.md)   
 [auto_gcroot Members](../vs140/auto_gcroot-Members.md)   
 [Handles in Native Types](../vs140/How-to--Declare-Handles-in-Native-Types.md)   
 [auto_handle Class](../vs140/auto_handle-Class.md)