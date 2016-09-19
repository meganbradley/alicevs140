---
title: "Dimension"
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
ms.assetid: 94f791da-bfea-454f-8a14-da31e8e1596a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Dimension
Each FORTRAN array has a dimension that is identified by a `SymTagDimension` symbol.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_lowerBound](../vs140/IDiaSymbol--get_lowerBound.md)|`IDiaSymbol*`|Lower bound of a FORTRAN array dimension.|  
|[lowerBoundId](../vs140/IDiaSymbol--get_lowerBoundId.md)|`DWORD`|ID of the lower-bound symbol.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagDimension` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[IDiaSymbol::get_upperBound](../vs140/IDiaSymbol--get_upperBound.md)|`IDiaSymbol*`|Upper bound of a FORTRAN array dimension.|  
|[upperBoundId](../vs140/IDiaSymbol--get_upperBoundId.md)|`DWORD`|ID of the upper-bound symbol.|  
  
## See Also  
 [ArrayType](../vs140/ArrayType.md)   
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)