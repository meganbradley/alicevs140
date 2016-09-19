---
title: "CHandle::operator ="
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
ms.assetid: 115b9c5f-cc92-4a09-b4d4-0d4a31406b89
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHandle::operator =
The assignment operator.  
  
## Syntax  
  
```  
  
      CHandle& operator =(   
   CHandle& h    
) throw( );  
```  
  
#### Parameters  
 `h`  
 `CHandle` will take ownership of the handle `h`.  
  
## Return Value  
 Returns a reference to the new `CHandle` object.  
  
## Remarks  
 If the `CHandle` object currently contains a handle, it will be closed. The `CHandle` object being passed in will have its handle reference set to NULL. This ensures that two `CHandle` objects will never contain the same active handle.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CHandle Class](../vs140/CHandle-Class.md)   
 [CHandle::Attach](../vs140/CHandle--Attach.md)