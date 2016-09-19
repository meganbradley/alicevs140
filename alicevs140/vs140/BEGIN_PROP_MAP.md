---
title: "BEGIN_PROP_MAP"
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
ms.assetid: bfe30be6-62c3-4dc2-bd49-21ef96f15427
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_PROP_MAP
Marks the beginning of the object's property map.  
  
## Syntax  
  
```  
  
BEGIN_PROP_MAP( theClass )  
```  
  
#### Parameters  
 `theClass`  
 [in] Specifies the class containing the property map.  
  
## Remarks  
 The property map stores property descriptions, property DISPIDs, property page CLSIDs, and `IDispatch` IIDs. Classes [IPerPropertyBrowsingImpl](../vs140/IPerPropertyBrowsingImpl-Class.md), [IPersistPropertyBagImpl](../vs140/IPersistPropertyBagImpl-Class.md), [IPersistStreamInitImpl](../vs140/IPersistStreamInitImpl-Class.md), and [ISpecifyPropertyPagesImpl](../vs140/ISpecifyPropertyPagesImpl-Class.md) use the property map to retrieve and set this information.  
  
 When you create an object with the ATL Project Wizard, the wizard will create an empty property map by specifying `BEGIN_PROP_MAP` followed by [END_PROP_MAP](../vs140/END_PROP_MAP.md).  
  
 `BEGIN_PROP_MAP` does not save out the extent (that is, the dimensions) of a property map, because an object using a property map may not have a user interface, so it would have no extent. If the object is an ActiveX control with a user interface, it has an extent. In this case, you must specify [PROP_DATA_ENTRY](../vs140/PROP_DATA_ENTRY.md) in your property map to supply the extent.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#103](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#103)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Property Map Macros](../vs140/Property-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)