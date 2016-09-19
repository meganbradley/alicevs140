---
title: "InlineIsEqualIUnknown"
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
ms.assetid: bb0be0a6-5b81-481d-856e-3aa076c69104
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# InlineIsEqualIUnknown
Call this function, for the special case of testing for **IUnknown**.  
  
## Syntax  
  
```  
  
      BOOL InlineIsEqualUnknown(  
   REFGUID rguid1   
);  
```  
  
#### Parameters  
 *rguid1*  
 [in] The GUID to compare to **IID_IUnknown**.  
  
## See Also  
 [COM Map Global Functions](../vs140/COM-Map-Global-Functions.md)