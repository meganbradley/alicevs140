---
title: "CComControlBase::m_bDrawFromNatural"
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
ms.assetid: 82af4d97-e139-421e-9859-d914cb1e80d9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_bDrawFromNatural
Flag indicating that `IDataObjectImpl::GetData` and `CComControlBase::GetZoomInfo` should set the control size from `m_sizeNatural` rather than from `m_sizeExtent`.  
  
## Syntax  
  
```  
  
unsigned m_bDrawFromNatural:1;  
```  
  
## Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [IDataObjectImpl::GetData](../vs140/IDataObjectImpl--GetData.md)   
 [CComControlBase::m_sizeNatural](../vs140/CComControlBase--m_sizeNatural.md)   
 [CComControlBase::m_sizeExtent](../vs140/CComControlBase--m_sizeExtent.md)