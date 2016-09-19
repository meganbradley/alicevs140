---
title: "_com_ptr_t::GetInterfacePtr"
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
ms.assetid: 55e3e2c7-c939-48b5-a905-4b9cbefeea7e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _com_ptr_t::GetInterfacePtr
**Microsoft Specific**  
  
 Returns the encapsulated interface pointer.  
  
## Syntax  
  
```  
  
      Interface* GetInterfacePtr( ) const throw( );   
Interface*& GetInterfacePtr() throw();  
```  
  
## Remarks  
 Returns the encapsulated interface pointer, which may be **NULL**.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_com_ptr_t Class](../vs140/_com_ptr_t-Class.md)