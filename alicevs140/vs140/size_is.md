---
title: "size_is"
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
ms.assetid: 70192d09-f6c5-4d52-b3fe-303f8cb10aa5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# size_is
Specify the size of memory allocated for sized pointers, sized pointers to sized pointers, and single- or multidimensional arrays.  
  
## Syntax  
  
```  
  
      [ size_is(  
   "expression"  
) ]  
```  
  
#### Parameters  
 *expression*  
 The size of memory allocated for sized pointers.  
  
## Remarks  
 The **size_is** C++ attribute has the same functionality as the [size_is](http://msdn.microsoft.com/library/windows/desktop/aa367164) MIDL attribute.  
  
## Example  
 See the example for [first_is](../vs140/first_is.md) for a sample of how to specify a section of an array.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Field in `struct` or **union**, interface parameter, interface method|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|**max_is**|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Typedef, Enum, Union, and Struct Attributes](../vs140/Typedef--Enum--Union--and-Struct-Attributes.md)   
 [Parameter Attributes](../vs140/Parameter-Attributes.md)   
 [first_is](../vs140/first_is.md)   
 [last_is](../vs140/last_is.md)   
 [max_is](../vs140/max_is.md)   
 [length_is](../vs140/length_is.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)