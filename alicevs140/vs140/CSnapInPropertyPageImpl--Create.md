---
title: "CSnapInPropertyPageImpl::Create"
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
ms.assetid: 053a3ba9-1ae9-4fe3-b9be-6dfcc729baa4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInPropertyPageImpl::Create
Call this function to initialize the underlying structure of the property page.  
  
## Syntax  
  
```  
  
HPROPSHEETPAGE Create( );  
  
```  
  
## Return Value  
 A handle to a **PROPSHEETPAGE** structure containing the attributes of the newly created property sheet.  
  
## Remarks  
 You should first call [CSnapInPropertyPageImpl::CSnapInPropertyPageImpl](../vs140/CSnapInPropertyPageImpl--CSnapInPropertyPageImpl.md) before calling this function.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInPropertyPageImpl Class](../vs140/CSnapInPropertyPageImpl-Class.md)