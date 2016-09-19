---
title: "ComPtrRefBase::operator IUnknown** Operator"
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
ms.assetid: c2950abf-a7aa-480a-ba41-615703e7f931
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtrRefBase::operator IUnknown** Operator
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
operator IUnknown**() const;  
```  
  
## Remarks  
 Casts the current [ptr_](../vs140/ComPtrRefBase--ptr_-Data-Member.md) data member to a pointer-to-a-pointer-to the IUnknown interface.  
  
 An error is emitted if the current ComPtrRefBase doesn't derive from IUnknown.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [ComPtrRefBase Class](../vs140/ComPtrRefBase-Class.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)