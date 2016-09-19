---
title: "AtlSetChildSite"
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
ms.assetid: 2a8ece19-6bfd-4e89-9d1d-e5a78f95e2df
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlSetChildSite
Call this function to set the site of the child object to the **IUnknown** of the parent object.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      HRESULT AtlSetChildSite(  
IUnknown* punkChild,  
IUnknown* punkParent   
);  
```  
  
#### Parameters  
 *punkChild*  
 [in] A pointer to the **IUnknown** interface of the child.  
  
 `punkParent`  
 [in] A pointer to the **IUnknown** interface of the parent.  
  
## Return Value  
 A standard HRESULT value.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [Composite Control Global Functions](../vs140/Composite-Control-Global-Functions.md)