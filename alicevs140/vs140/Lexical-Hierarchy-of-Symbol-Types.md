---
title: "Lexical Hierarchy of Symbol Types"
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
ms.assetid: 912da653-ddfe-45a4-84aa-64281283739a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Lexical Hierarchy of Symbol Types
The following table shows the symbol types in the lexical hierarchy.  
  
## Symbol Types  
  
|Symbol type|Description|  
|-----------------|-----------------|  
|[Annotation](../vs140/Annotation.md)|Specifies an annotated location in program code.|  
|[Block](../vs140/Block.md)|Specifies nested scopes in functions.|  
|`Compiland`|Specifies a `compiland` linked to the .exe file.|  
|[CompilandDetails](../vs140/CompilandDetails.md)|Specifies compiland data that may require loading additional compiland details and thus incur run-time overhead to retrieve.|  
|[CompilandEnv](../vs140/CompilandEnv.md)|Specifies any additional environment variables significant to the compilation of the compiland.|  
|[Custom (Debug Interface Access SDK)](../vs140/Custom--Debug-Interface-Access-SDK-.md)|Specifies a user-defined symbol.|  
|[Data (Debug Interface Access SDK)](../vs140/Data--Debug-Interface-Access-SDK-.md)|Specifies such variables as parameters, local variables, global variables, and class members.|  
|[Exe](../vs140/Exe.md)|Specifies the global scope of the data; corresponds to an entire .exe or .dll file.|  
|[FuncDebugEnd](../vs140/FuncDebugEnd.md)|Specifies a function that has a defined point at which debugging is to end.|  
|[FuncDebugStart](../vs140/FuncDebugStart.md)|Specifies a function that has a defined point at which debugging is to begin.|  
|[Function (Debug Interface Access SDK)](../vs140/Function--Debug-Interface-Access-SDK-.md)|Specifies a function.|  
|[Label (Debug Interface Access SDK)](../vs140/Label--Debug-Interface-Access-SDK-.md)|Specifies a location in program code.|  
|[PublicSymbol](../vs140/PublicSymbol.md)|Specifies an external symbol that appears when building the executable program.|  
|[Thunk](../vs140/Thunk.md)|Specifies a `thunk`.|  
|[UsingNameSpace](../vs140/UsingNameSpace.md)|Specifies a `namespace`identifier.|  
  
> [!NOTE]
>  Additional symbol properties may be available depending on the symbol type. These properties are listed in the individual symbol topics.  
  
## See Also  
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)   
 [IDiaSymbol::get_symTag](../vs140/IDiaSymbol--get_symTag.md)   
 [Symbols and Symbol Tags](../vs140/Symbols-and-Symbol-Tags.md)   
 [SymTagEnum Enumeration](../vs140/SymTagEnum.md)