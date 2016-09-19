---
title: "VCPROFILE_ALLOC_SCALE"
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
ms.assetid: 5cb5ce27-f9b8-489b-b46c-d6e9bcab2d34
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# VCPROFILE_ALLOC_SCALE
Modify the amount of memory allocated to hold the profile data.  
  
## Syntax  
  
```  
VCPROFILE_ALLOC_SCALE=scale_value  
```  
  
#### Parameters  
 `scale_value`  
 The scale value for the amount of memory you want for running test scenarios.  The default is 1.  
  
## Remarks  
 In rare cases, there will not be enough memory available to support gathering profile data when running test scenarios.  In those cases, you can increase the amount of memory with `VCPROFILE_ALLOC_SCALE`.  
  
 If you receive an error message during a test run that indicates that you have insufficient memory, assign a larger value to `VCPROFILE_ALLOC_SCALE`, until the test runs complete with no out-of-memory errors.  
  
## Example  
  
```  
set VCPROFILE_ALLOC_SCALE=2  
```  
  
## See Also  
 [Environment Variables for Profile-Guided Optimizations](../vs140/Environment-Variables-for-Profile-Guided-Optimizations.md)