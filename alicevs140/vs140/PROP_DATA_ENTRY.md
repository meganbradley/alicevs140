---
title: "PROP_DATA_ENTRY"
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
ms.assetid: 9488b68a-4744-42c0-bf56-c21846f84d55
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PROP_DATA_ENTRY
Indicates the extent, or dimensions, of an ActiveX control.  
  
## Syntax  
  
```  
  
      PROP_DATA_ENTRY(   
   szDesc,   
   member,   
   vt    
)  
```  
  
#### Parameters  
 `szDesc`  
 [in] The property description.  
  
 `member`  
 [in] The data member containing the extent; for example, `m_sizeExtent`.  
  
 *vt*  
 [in] Specifies the VARIANT type of the property.  
  
## Remarks  
 This macro causes the specified data member to be persisted.  
  
 When you create an ActiveX control, the wizard inserts this macro after the property map macro [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md) and before the property map macro [END_PROP_MAP](../vs140/END_PROP_MAP.md).  
  
## Example  
 In the following example, the extent of the object (`m_sizeExtent`) is being persisted.  
  
 [!CODE [NVC_ATL_Windowing#131](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#131)]  
  
 [!CODE [NVC_ATL_Windowing#132](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#132)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Property Map Macros](../vs140/Property-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)