---
title: "auto_ptr::operator*"
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
ms.assetid: cac925f2-86e7-4d03-8ca3-545d3d95bd02
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_ptr::operator*
The dereferencing operator for objects of type `auto_ptr`.  
  
## Syntax  
  
```  
  
Type& operator*( ) const throw( );  
  
```  
  
## Return Value  
 A reference to an object of type **Type** that the pointer owns.  
  
## Remarks  
 The indirection operator returns `*`[get](../vs140/auto_ptr--get.md). Hence, the stored pointer must not be null.  
  
## Example  
 For an example of how to use the member function, see [auto_ptr::auto_ptr](../vs140/auto_ptr--auto_ptr.md).  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [auto_ptr Class](../vs140/auto_ptr-Class.md)