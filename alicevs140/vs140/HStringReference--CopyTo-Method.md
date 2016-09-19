---
title: "HStringReference::CopyTo Method"
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
ms.assetid: 179d9b14-1ced-4b16-b297-19ca1e92a462
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HStringReference::CopyTo Method
Copies the current HStringReference object to an HSTRING object.  
  
## Syntax  
  
```  
  
HRESULT CopyTo(  
   _Out_ HSTRING *str  
   ) const throw();  
```  
  
#### Parameters  
 `str`  
 The HSTRING that receives the copy.  
  
## Remarks  
 This method calls the [WindowsDuplicateString](http://msdn.microsoft.com/library/br224634.aspx) function.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [HStringReference Class](../vs140/HStringReference-Class.md)