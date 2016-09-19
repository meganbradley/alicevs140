---
title: "_com_ptr_t::Detach"
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
ms.topic: language-reference
ms.assetid: 0652053e-af37-44e9-a278-2522212ebfed
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _com_ptr_t::Detach
**Microsoft Specific**  
  
 Extracts and returns the encapsulated interface pointer.  
  
## Syntax  
  
```  
  
Interface* Detach( ) throw( );  
  
```  
  
## Remarks  
 Extracts and returns the encapsulated interface pointer, and then clears the encapsulated pointer storage to **NULL**. This removes the interface pointer from encapsulation. It is up to you to call **Release** on the returned interface pointer.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_com_ptr_t Class](../vs140/_com_ptr_t-Class.md)