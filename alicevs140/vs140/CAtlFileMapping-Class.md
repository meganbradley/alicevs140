---
title: "CAtlFileMapping Class"
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
ms.assetid: 899fc058-e05e-48b5-aca9-340403bb9e26
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFileMapping Class
This class represents a memory-mapped file, adding a cast operator to the methods of [CAtlFileMappingBase](../vs140/CAtlFileMappingBase-Class.md).  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template <  
   typename  T  
   = char>  
   class CAtlFileMapping :  
   public CAtlFileMappingBase  
  
```  
  
#### Parameters  
 `T`  
 The type of data used for the cast operator.  
  
## Members  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlFileMapping::operator T*](../vs140/CAtlFileMapping--operator-T-.md)|Allows implicit conversion of `CAtlFileMapping` objects to `T`**\***.|  
  
## Remarks  
 This class adds a single cast operator to allow implicit conversion of `CAtlFileMapping` objects to `T`**\***. Other members are supplied by the base class, [CAtlFileMappingBase](../vs140/CAtlFileMappingBase-Class.md).  
  
## Inheritance Hierarchy  
 [CAtlFileMappingBase](../vs140/CAtlFileMappingBase-Class.md)  
  
 `CAtlFileMapping`  
  
## Requirements  
 **Header:** atlfile.h  
  
##  <a name="catlfilemapping__operator_t_star"></a>  CAtlFileMapping::operator T*  
 Allows implicit conversion of `CAtlFileMapping` objects to `T`**\***.  
  
```  
  
operator T*() const throw( );  
  
```  
  
### Return Value  
 Returns a `T`**\*** pointer to the start of the memory-mapped file.  
  
### Remarks  
 Calls [CAtlFileMappingBase::GetData](../vs140/CAtlFileMappingBase--GetData.md) and reinterprets the returned pointer as a `T`**\*** where *T* is the type used as the template parameter of this class.  
  
## See Also  
 [CAtlFileMappingBase Class](../vs140/CAtlFileMappingBase-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)