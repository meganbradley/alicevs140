---
title: "CComControlBase::m_bAutoSize"
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
ms.assetid: e22ae270-5ecc-451d-9dba-e9824fa1b5eb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_bAutoSize
Flag indicating the control cannot be any other size.  
  
## Syntax  
  
```  
  
unsigned m_bAutoSize:1;  
```  
  
## Remarks  
 This flag is checked by `IOleObjectImpl::SetExtent` and, if **TRUE**, causes the function to return **E_FAIL**.  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 If you add the **Auto Size** option on the [Stock Properties](../vs140/Stock-Properties--ATL-Control-Wizard.md) tab of the ATL Control Wizard, the wizard automatically creates this data member in your control class, creates put and get methods for the property, and supports [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638) to automatically notify the container when the property changes.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [IOleObjectImpl::SetExtent](../vs140/IOleObjectImpl--SetExtent.md)