---
title: "AFX_GLOBAL_DATA::IsWindowsLayerSupportAvailable"
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
ms.assetid: 4734cee5-9fba-4f99-8315-b67d3da3b6d3
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_GLOBAL_DATA::IsWindowsLayerSupportAvailable
Indicates whether the operating system supports layered windows.  
  
## Syntax  
  
```  
BOOL IsWindowsLayerSupportAvailable() const;  
```  
  
## Return Value  
 `TRUE` if layered windows are supported; otherwise, `FALSE`.  
  
## Remarks  
 If layered windows are supported, *smart docking* markers use layered windows.  
  
## Requirements  
 **Header:** afxglobals.h  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)