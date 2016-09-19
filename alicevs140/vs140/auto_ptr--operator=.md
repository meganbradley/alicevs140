---
title: "auto_ptr::operator="
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
ms.assetid: b2be6646-adf6-4588-b890-cf50f0a58e14
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_ptr::operator=
An assignment operator that transfers ownership from one `auto_ptr` object to another.  
  
## Syntax  
  
```  
template<class Other>  
   auto_ptr<Type>& operator=(  
      auto_ptr<Other>& _Right  
   ) throw( );  
auto_ptr<Type>& operator=(  
   auto_ptr<Type>& _Right  
) throw( );  
auto_ptr<Type>& operator=(  
   auto_ptr_ref<Type> _Right  
) throw( );  
```  
  
#### Parameters  
 `_Right`  
 An object of type `auto_ptr`.  
  
## Return Value  
 A reference to an object of type `auto_ptr`<**Type**>.  
  
## Remarks  
 The assignment evaluates the expression **delete myptr**, but only if the stored pointer **myptr** changes as a result of the assignment. It then transfers ownership of the pointer stored in _*Right*, by storing \_*Right*.[release](../vs140/auto_ptr--release.md) in **myptr**. The function returns **\*this**.  
  
## Example  
 For an example of the use of the member operator, see [auto_ptr::auto_ptr](../vs140/auto_ptr--auto_ptr.md).  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [auto_ptr Class](../vs140/auto_ptr-Class.md)