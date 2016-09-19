---
title: "random_device::random_device"
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
ms.assetid: 3e4d021d-e50b-40bc-ae29-9071d7e5cd38
caps.latest.revision: 20
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# random_device::random_device
Constructs the generator.  
  
## Syntax  
  
```  
random_device(const std::string& = "");  
```  
  
## Remarks  
 The constructor initializes the generator as needed, ignoring the string parameter. Throws a value of an implementation-defined type derived from [exception](../vs140/exception-Class.md) if the `random_device` could not be initialized.  
  
 For example code, see [random_device](../vs140/random_device-Class.md).  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [random_device](../vs140/random_device-Class.md)