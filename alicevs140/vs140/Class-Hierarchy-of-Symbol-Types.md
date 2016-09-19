---
title: "Class Hierarchy of Symbol Types"
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
ms.assetid: 0ccd6990-4654-44cd-a6f3-bdd82fe90f6c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Class Hierarchy of Symbol Types
The following table describes the symbol types in the class hierarchy.  
  
## Symbol Types  
  
|Symbol type|Description|  
|-----------------|-----------------|  
|[UDT](../vs140/UDT.md)|Symbol used to represent each class, structure, and union.|  
|[Enum (Debug Interface Access SDK)](../vs140/Enum--Debug-Interface-Access-SDK-.md)|Symbol for enumerated types.|  
|[PointerType](../vs140/PointerType.md)|Symbol for pointer types.|  
|[ArrayType](../vs140/ArrayType.md)|Symbol for array types.|  
|[BaseType](../vs140/BaseType.md)|Symbol for base types|  
|[Typedef (Debug Interface Access SDK)](../vs140/Typedef--Debug-Interface-Access-SDK-.md)|Symbol that introduces names for other types.|  
|[BaseClass](../vs140/BaseClass.md)|Symbol used for each base class of a user-defined type (UDT).|  
|[Friend (Debug Interface Access SDK)](../vs140/Friend--Debug-Interface-Access-SDK-.md)|Symbol for friend classes and friend functions.|  
|[FunctionType](../vs140/FunctionType.md)|Symbol for each unique function signature.|  
|[FunctionArgType](../vs140/FunctionArgType.md)|Symbol for each parameter to a function.|  
|[VTableShape](../vs140/VTableShape.md)|Symbol for the size of the virtual table.|  
|[VTable](../vs140/VTable.md)|Symbol for a virtual table.|  
|[CustomType](../vs140/CustomType.md)|Symbol for vendor-defined type.|  
|[ManagedType](../vs140/ManagedType.md)|Symbol for a type defined in metadata.|  
|[Dimension](../vs140/Dimension.md)|Symbol for array dimensions.|  
  
> [!NOTE]
>  Each symbol can have properties that hold information about the symbol, as well as references to other symbols. These properties are listed in the individual symbol topics.  
  
## See Also  
 [CV_access_e Enumeration](../vs140/CV_access_e.md)   
 [Lexical Hierarchy of Symbol Types](../vs140/Lexical-Hierarchy-of-Symbol-Types.md)   
 [Symbols and Symbol Tags](../vs140/Symbols-and-Symbol-Tags.md)