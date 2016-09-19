---
title: "IDiaSymbol::get_numberOfAcceleratorPointerTags"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1886e3ec-b227-4187-8d93-c5144b4b77ae
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_numberOfAcceleratorPointerTags
Returns the number of accelerator pointer tags in a C++ AMP stub function.  
  
## Syntax  
  
```cpp  
HRESULT get_numberOfAcceleratorPointerTags(   
   DWORD* count);  
```  
  
#### Parameters  
 `count`  
 [out] A pointer to a `DWORD` that holds the number of accelerator pointer tags in a C++ AMP stub function.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
## Remarks  
 This method is called on an `IDiaSymbol` interface that corresponds to a C++ AMP accelerator stub function.  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)