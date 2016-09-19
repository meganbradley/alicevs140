---
title: "COM_INTERFACE_ENTRY (ATL)"
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
ms.assetid: c5363b8b-a1a2-471e-ad3a-d472f6c356c5
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY (ATL)
Enters interfaces into the COM interface map.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY(   
x  
 )  
  
```  
  
#### Parameters  
 *x*  
 [in] The name of an interface your class object derives from directly.  
  
## Remarks  
 Typically, this is the entry type you use most often.  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#109](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#109)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)