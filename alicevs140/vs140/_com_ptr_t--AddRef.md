---
title: "_com_ptr_t::AddRef"
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
ms.assetid: c104dac3-aad3-40bb-a298-75c6cd0e63a2
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _com_ptr_t::AddRef
**Microsoft Specific**  
  
 Calls the `AddRef` member function of **IUnknown** on the encapsulated interface pointer.  
  
## Syntax  
  
```  
  
void AddRef( );  
  
```  
  
## Remarks  
 Calls `IUnknown::AddRef` on the encapsulated interface pointer, raising an `E_POINTER` error if the pointer is **NULL**.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_com_ptr_t Class](../vs140/_com_ptr_t-Class.md)