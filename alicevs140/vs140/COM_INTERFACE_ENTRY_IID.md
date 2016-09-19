---
title: "COM_INTERFACE_ENTRY_IID"
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
ms.assetid: 1bb69549-2099-4e20-ad5e-4c5a32f44e4b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_IID
Use this macro to enter the interface into the COM map and specify its IID.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_IID(   
iid  
,   
x  
 )  
  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID of the interface exposed.  
  
 *x*  
 [in] The name of the class whose vtable will be exposed as the interface identified by `iid`.  
  
## Remarks  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#117](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#117)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)