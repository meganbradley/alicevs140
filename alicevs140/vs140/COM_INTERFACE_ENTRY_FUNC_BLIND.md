---
title: "COM_INTERFACE_ENTRY_FUNC_BLIND"
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
ms.assetid: 8443ca59-72e6-4cec-ae91-266be0db12db
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_FUNC_BLIND
Same as [COM_INTERFACE_ENTRY_FUNC](../vs140/COM_INTERFACE_ENTRY_FUNC.md), except that querying for any IID results in a call to `func`.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_FUNC_BLIND(   
dw  
,   
func  
 )  
  
```  
  
#### Parameters  
 `dw`  
 [in] A parameter passed through to the `func`.  
  
 `func`  
 [in] The function that gets called when this entry in the COM map is processed.  
  
## Remarks  
 Any failure will cause processing to continue on the COM map. If the function returns an interface pointer, it should return `S_OK`.  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)