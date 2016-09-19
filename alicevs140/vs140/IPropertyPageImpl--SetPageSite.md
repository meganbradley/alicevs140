---
title: "IPropertyPageImpl::SetPageSite"
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
ms.assetid: 92ac1313-50db-4670-bf55-ab384204f50e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPropertyPageImpl::SetPageSite
Provides the property page with an [IPropertyPageSite](http://msdn.microsoft.com/library/windows/desktop/ms690583) pointer, through which the property page communicates with the property frame.  
  
## Syntax  
  
```  
  
      HRESULT SetPageSite(  
   IPropertyPageSite* pPageSite   
);  
```  
  
## Remarks  
 See [IPropertyPage::SetPageSite](http://msdn.microsoft.com/library/windows/desktop/ms690413) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPropertyPageImpl Class](../vs140/IPropertyPageImpl-Class.md)   
 [IPropertyPageImpl::m_pPageSite](../vs140/IPropertyPageImpl--m_pPageSite.md)   
 [IPropertyPageSite](http://msdn.microsoft.com/library/windows/desktop/ms690583)