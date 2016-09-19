---
title: "IPropertyPageImpl::SetDirty"
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
ms.assetid: a7510487-5db6-4940-be4e-e07b2ef4da8b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPropertyPageImpl::SetDirty
Flags the property page's state as changed or unchanged, depending on the value of `bDirty`.  
  
## Syntax  
  
```  
  
      void SetDirty(  
   BOOL bDirty   
);  
```  
  
#### Parameters  
 `bDirty`  
 [in] If **TRUE**, the property page's state is marked as changed. Otherwise, it is marked as unchanged.  
  
## Remarks  
 If necessary, `SetDirty` informs the frame that the property page has changed.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPropertyPageImpl Class](../vs140/IPropertyPageImpl-Class.md)   
 [IPropertyPageImpl::IsPageDirty](../vs140/IPropertyPageImpl--IsPageDirty.md)   
 [IPropertyPageImpl::SetPageSite](../vs140/IPropertyPageImpl--SetPageSite.md)   
 [IPropertyPageImpl::m_bDirty](../vs140/IPropertyPageImpl--m_bDirty.md)