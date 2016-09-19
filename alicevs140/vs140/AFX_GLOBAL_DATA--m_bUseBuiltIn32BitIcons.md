---
title: "AFX_GLOBAL_DATA::m_bUseBuiltIn32BitIcons"
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
ms.topic: article
ms.assetid: 43b074ff-7761-4a82-bc0e-0e9f98119ea6
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_GLOBAL_DATA::m_bUseBuiltIn32BitIcons
Indicates whether the framework uses predefined 32-bit color icons or icons of a lower resolution.  
  
## Syntax  
  
```  
BOOL  m_bUseBuiltIn32BitIcons;  
```  
  
## Remarks  
 `TRUE` specifies that the framework use 32-bit color icons; `FALSE` specifies lower resolution icons. The `AFX_GLOBAL_DATA::AFX_GLOBAL_DATA` constructor initializes this member to `TRUE`.  
  
 This member must be set at application startup.  
  
## Requirements  
 **Header:** afxglobals.h  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)