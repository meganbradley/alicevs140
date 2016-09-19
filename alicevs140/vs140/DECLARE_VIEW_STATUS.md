---
title: "DECLARE_VIEW_STATUS"
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
ms.assetid: 21c27c4b-96d7-4320-a185-c8ce9c7811fc
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_VIEW_STATUS
Place this macro in an ATL ActiveX control's control class to specify the **VIEWSTATUS** flags to the container.  
  
## Syntax  
  
```  
  
      DECLARE_VIEW_STATUS(   
   statusFlags    
)  
```  
  
#### Parameters  
 `statusFlags`  
 [in] The **VIEWSTATUS** flags. See [VIEWSTATUS](http://msdn.microsoft.com/library/windows/desktop/ms687201) for a list of flags.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#126](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#126)]  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)