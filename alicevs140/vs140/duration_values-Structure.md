---
title: "duration_values Structure"
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
ms.assetid: 7f66d2e3-1faf-47c3-b47e-08f2a87f20e8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# duration_values Structure
Provides specific values for the [duration](../vs140/duration-Class.md) template parameter `Rep`.  
  
## Syntax  
  
```  
template<class Rep>  
   struct duration_values;  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[duration_values::max Method](#duration_values__max_method)|Static. Specifies the upper limit for a value of type `Rep`.|  
|[duration_values::min Method](#duration_values__min_method)|Static. Specifies the lower limit for a value of type `Rep`.|  
|[duration_values::zero Method](#duration_values__zero_method)|Static. Returns `Rep(0)`.|  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
##  <a name="duration_values__max_method"></a>  duration_values::max Method  
 Static method that returns the upper bound for values of type `Ref`.  
  
```  
static constexpr Rep max();  
```  
  
### Return Value  
 In effect, returns `numeric_limits<Rep>::max()`.  
  
### Remarks  
 When `Rep` is a user-defined type, the return value must be greater than [duration_values::zero](#duration_values__zero_method).  
  
##  <a name="duration_values__min_method"></a>  duration_values::min Method  
 Static method that returns the lower bound for values of type `Ref`.  
  
```  
static constexpr Rep min();  
```  
  
### Return Value  
 In effect, returns `numeric_limits<Rep>::lowest()`.  
  
### Remarks  
 When `Rep` is a user-defined type, the return value must be less than or equal to [duration_values::zero](#duration_values__zero_method).  
  
##  <a name="duration_values__zero_method"></a>  duration_values::zero Method  
 Returns `Rep(0)`.  
  
```  
static constexpr Rep zero();  
```  
  
### Remarks  
 When `Rep` is a user-defined type, the return value must represent the additive infinity.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<chrono\>](../vs140/-chrono-.md)