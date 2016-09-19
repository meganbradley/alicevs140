---
title: "auto_ptr::operator-&gt;"
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
ms.assetid: b71aecd6-7ab1-4629-a532-328cad8523e1
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_ptr::operator-&gt;
The operator for allowing member access.  
  
## Syntax  
  
```  
  
Type *operator->( ) const throw( );  
  
```  
  
## Return Value  
 A member of the object that **auto_ptr** owns.  
  
## Remarks  
 The selection operator returns [get](../vs140/auto_ptr--get.md)`( )`, so that the expression *ap*->**member** behaves the same as ( *ap*.**get**( ) )->**member**, where *ap* is an object of class `auto_ptr`<**Type**>. Hence, the stored pointer must not be null, and **Type** must be a class, struct, or union type with a **member** member.  
  
## Example  
 For an example of how to use the member function, see [auto_ptr::auto_ptr](../vs140/auto_ptr--auto_ptr.md).  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [auto_ptr Class](../vs140/auto_ptr-Class.md)