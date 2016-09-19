---
title: "PROP_PAGE"
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
ms.assetid: 2155973e-b96c-4385-bf85-5d6112c969b8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PROP_PAGE
Use this macro to enter a property page CLSID into the object's property map.  
  
## Syntax  
  
```  
  
      PROP_PAGE(   
   clsid    
)  
```  
  
#### Parameters  
 `clsid`  
 [in] The CLSID of a property page.  
  
## Remarks  
 `PROP_PAGE` is similar to [PROP_ENTRY_TYPE](../vs140/PROP_ENTRY_TYPE.md), but does not require a property description or DISPID.  
  
> [!NOTE]
>  If you have already entered a CLSID with `PROP_ENTRY_TYPE` or [PROP_ENTRY_TYPE_EX](../vs140/PROP_ENTRY_TYPE_EX.md), you do not need to make an additional entry with `PROP_PAGE`.  
  
 The [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md) macro marks the beginning of the property map; the [END_PROP_MAP](../vs140/END_PROP_MAP.md) macro marks the end.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#134](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#134)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Property Map Macros](../vs140/Property-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)