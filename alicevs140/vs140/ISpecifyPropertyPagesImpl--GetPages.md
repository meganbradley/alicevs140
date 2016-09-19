---
title: "ISpecifyPropertyPagesImpl::GetPages"
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
ms.assetid: ff622261-5df2-4192-8dbf-264092138ab3
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ISpecifyPropertyPagesImpl::GetPages
Fills the array in the [CAUUID](http://msdn.microsoft.com/library/windows/desktop/ms680048) structure with the CLSIDs for the property pages that can be displayed in the object's property sheet.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetPages)(  
   CAUUID* pPages   
);  
```  
  
## Remarks  
 ATL uses the object's property map to retrieve each CLSID.  
  
 See [ISpecifyPropertyPages::GetPages](http://msdn.microsoft.com/library/windows/desktop/ms687276) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [ISpecifyPropertyPagesImpl Class](../vs140/ISpecifyPropertyPagesImpl-Class.md)   
 [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md)