---
title: "COM_INTERFACE_ENTRY_CACHED_TEAR_OFF"
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
ms.assetid: 195d37df-1ae1-4ac5-b5f1-294ad652189a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_CACHED_TEAR_OFF
Saves the interface-specific data for every instance.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_CACHED_TEAR_OFF(   
iid  
,   
x  
,   
punk  
 )  
  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID of the tear-off interface.  
  
 *x*  
 [in] The name of the class implementing the interface.  
  
 `punk`  
 [in] The name of an **IUnknown** pointer. Must be a member of the class containing the COM map. Should be initialized to **NULL** in the class object's constructor.  
  
## Remarks  
 If the interface is not used, this lowers the overall instance size of your object.  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Example  
 [!CODE [NVC_ATL_COM#54](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#54)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)