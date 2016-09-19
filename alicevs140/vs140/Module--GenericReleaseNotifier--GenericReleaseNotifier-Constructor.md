---
title: "Module::GenericReleaseNotifier::GenericReleaseNotifier Constructor"
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
ms.assetid: feb5b687-a4b0-4809-9022-8f292181b7a1
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module::GenericReleaseNotifier::GenericReleaseNotifier Constructor
Initializes a new instance of the Module::GenericReleaseNotifier class.  
  
## Syntax  
  
```  
  
      GenericReleaseNotifier(  
   T callback,   
   bool release  
) throw() : ReleaseNotifier(release), callback_(callback);  
```  
  
#### Parameters  
 `callback`  
 A lambda, functor, or pointer-to-function event handler that can be invoked with the parentheses function operator (`()`).  
  
 `release`  
 Specify `true` to enable calling the underlying [Module::ReleaseNotifier::Release()](../vs140/Module--ReleaseNotifier--Release.md) method; otherwise, specify `false`.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Module::GenericReleaseNotifier Class](../vs140/Module--GenericReleaseNotifier-Class.md)