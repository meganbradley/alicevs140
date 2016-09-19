---
title: "IPropertyPageImpl::SetObjects"
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
ms.assetid: 1ddb75b7-5944-4c55-bdb2-79c3e088f898
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPropertyPageImpl::SetObjects
Provides an array of **IUnknown** pointers for the objects associated with the property page.  
  
## Syntax  
  
```  
  
      HRESULT SetObjects(  
   ULONG nObjects,  
   IUnknown** ppUnk   
);  
```  
  
## Remarks  
 See [IPropertyPage::SetObjects](http://msdn.microsoft.com/library/windows/desktop/ms678529) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPropertyPageImpl Class](../vs140/IPropertyPageImpl-Class.md)   
 [IPropertyPageImpl::Apply](../vs140/IPropertyPageImpl--Apply.md)   
 [IPropertyPageImpl::m_nObjects](../vs140/IPropertyPageImpl--m_nObjects.md)   
 [IPropertyPageImpl::m_ppUnk](../vs140/IPropertyPageImpl--m_ppUnk.md)