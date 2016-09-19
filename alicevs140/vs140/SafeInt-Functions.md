---
title: "SafeInt Functions"
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
ms.topic: language-reference
ms.assetid: fdc208e5-5d8a-41a9-8271-567fd438958d
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SafeInt Functions
The SafeInt library provides several functions that you can use without creating an instance of the [SafeInt Class](../vs140/SafeInt-Class.md). If you want to protect a single mathematical operation from integer overflow, you can use these functions. If you want to protect multiple mathematical operations, you should create `SafeInt` objects. It is more efficient to create `SafeInt` objects than to use these functions multiple times.  
  
 These functions enable you to compare or perform mathematical operations on two different types of parameters without having to convert them to the same type first.  
  
 Each of these functions has two template types: `T` and `U`. Each of these types can be a Boolean, character, or integral type. Integral types can be signed or unsigned and any size from 8 bits to 64 bits.  
  
## In This Section  
  
|Function|Description|  
|--------------|-----------------|  
|[SafeAdd](../vs140/SafeAdd.md)|Adds two numbers and protects against overflow.|  
|[SafeCast](../vs140/SafeCast.md)|Casts one type of parameter to another type.|  
|[SafeDivide](../vs140/SafeDivide.md)|Divides two numbers and protects against dividing by zero.|  
|[SafeEquals](../vs140/SafeEquals.md), [SafeGreaterThan](../vs140/SafeGreaterThan.md), [SafeGreaterThanEquals](../vs140/SafeGreaterThanEquals.md), [SafeLessThan](../vs140/SafeLessThan.md), [SafeLessThanEquals](../vs140/SafeLessThanEquals.md), [SafeNotEquals](../vs140/SafeNotEquals.md)|Compares two numbers. These functions enable you to compare two different types of numbers without changing their types.|  
|[SafeModulus](../vs140/SafeModulus.md)|Performs the modulus operation on two numbers.|  
|[SafeMultiply](../vs140/SafeMultiply.md)|Multiplies two numbers together and protects against overflow.|  
|[SafeSubtract](../vs140/SafeSubtract.md)|Subtracts two numbers and protects against overflow.|  
  
## Related Sections  
  
|Section|Description|  
|-------------|-----------------|  
|[SafeInt Class](../vs140/SafeInt-Class.md)|The `SafeInt` class.|  
|[SafeIntException Class](../vs140/SafeIntException-Class.md)|The exception class specific to the SafeInt library.|