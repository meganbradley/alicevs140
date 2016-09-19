---
title: "IPropertyPageImpl::GetPageInfo"
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
ms.assetid: da86a81f-cf0e-4292-9811-bec7dc32faa9
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPropertyPageImpl::GetPageInfo
Fills the *pPageInfo* structure with information contained in the data members.  
  
## Syntax  
  
```  
  
      HRESULT GetPageInfo(  
   PROPPAGEINFO* pPageInfo   
);  
```  
  
## Remarks  
 `GetPageInfo` loads the string resources associated with [m_dwDocString](../vs140/IPropertyPageImpl--m_dwDocString.md), [m_dwHelpFile](../vs140/IPropertyPageImpl--m_dwHelpFile.md), and [m_dwTitle](../vs140/IPropertyPageImpl--m_dwTitle.md).  
  
 See [IPropertyPage::GetPageInfo](http://msdn.microsoft.com/library/windows/desktop/ms680714) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPropertyPageImpl Class](../vs140/IPropertyPageImpl-Class.md)   
 [IPropertyPageImpl::m_dwHelpContext](../vs140/IPropertyPageImpl--m_dwHelpContext.md)   
 [IPropertyPageImpl::m_size](../vs140/IPropertyPageImpl--m_size.md)   
 [PROPPAGEINFO](http://msdn.microsoft.com/library/windows/desktop/ms680584)