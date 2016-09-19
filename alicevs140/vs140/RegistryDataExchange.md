---
title: "RegistryDataExchange"
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
ms.assetid: 2a201593-4d9e-429f-94a3-3c01601fbab6
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RegistryDataExchange
This function is called to read from, or write to, the system registry.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      HRESULT RegistryDataExchange(  
T* pT,  
enum RDXOperations rdxOp,  
void* pItem= NULL   
);  
```  
  
#### Parameters  
 *pT*  
 A pointer to the current object.  
  
 *rdxOp*  
 An enum value that indicates which operation the function should perform. See the table in the Remarks section for the allowed values.  
  
 `pItem`  
 Pointer to the data that is to be read from, or written to, the registry. The data can also represent a key to be deleted from the registry. The default value is NULL.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 The macros [BEGIN_RDX_MAP](../vs140/BEGIN_RDX_MAP.md) and [END_RDX_MAP](../vs140/END_RDX_MAP.md) expand to a function that calls `RegistryDataExchange`.  
  
 The possible enum values that indicate the operation the function should perform are shown in the following table:  
  
|Enum value|Operation|  
|----------------|---------------|  
|eReadFromReg|Read data from the registry.|  
|eWriteToReg|Write data to the registry.|  
|eDeleteFromReg|Delete the key from the registry.|  
  
## See Also  
 [Registry and TypeLib Global Functions](../vs140/Registry-and-TypeLib-Global-Functions.md)   
 [Registry Data Exchange Macros](../vs140/Registry-Data-Exchange-Macros.md)