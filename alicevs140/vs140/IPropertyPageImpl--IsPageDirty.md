---
title: "IPropertyPageImpl::IsPageDirty"
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
ms.assetid: e4171cfc-082e-4c62-934a-41409d2484e9
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPropertyPageImpl::IsPageDirty
Indicates whether the property page has changed since it was activated.  
  
## Syntax  
  
```  
HRESULT IsPageDirty(  
void   
);  
```  
  
## Remarks  
 `IsPageDirty` returns `S_OK` if the page has changed since it was activated.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPropertyPageImpl Class](../vs140/IPropertyPageImpl-Class.md)   
 [IPropertyPageImpl::SetDirty](../vs140/IPropertyPageImpl--SetDirty.md)   
 [IPropertyPageImpl::m_bDirty](../vs140/IPropertyPageImpl--m_bDirty.md)