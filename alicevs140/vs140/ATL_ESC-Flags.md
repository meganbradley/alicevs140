---
title: "ATL_ESC Flags"
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
ms.assetid: daf3aa3c-7498-4d63-9fb6-e05b4815c2b8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL_ESC Flags
These flags are used to control the behavior of [EscapeXML](../vs140/EscapeXML.md).  
  
## Syntax  
  
```  
  
      #define ATL_ESC_FLAG_NONE   
#define ATL_ESC_FLAG_ATTR  
```  
  
## Remarks  
  
|Flag|Description|  
|----------|-----------------|  
|ATL_ESC_FLAG_NONE|Default behavior. Quote marks and apostrophes are not converted.|  
|ATL_ESC_FLAG_ATTR|Quote marks and apostrophes are converted to &quot; and &apos; respectively.|  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Macros Alphabetical Reference](../vs140/ATL-Macros-Alphabetical-Reference.md)   
 [EscapeXML](../vs140/EscapeXML.md)