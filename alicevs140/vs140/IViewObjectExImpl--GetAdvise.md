---
title: "IViewObjectExImpl::GetAdvise"
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
ms.assetid: 2fd650fb-7907-44d9-a31a-36d4bafa9f4e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IViewObjectExImpl::GetAdvise
Retrieves an existing advisory sink connection on the control, if there is one.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetAdvise)(  
   DWORD* /* pAspects */,  
   DWORD* /* pAdvf */,  
   IAdviseSink** /* ppAdvSink */  
);  
```  
  
## Remarks  
 The advisory sink is stored in the control class data member [CComControlBase::m_spAdviseSink](../vs140/CComControlBase--m_spAdviseSink.md).  
  
 See [IViewObject::GetAdvise](http://msdn.microsoft.com/library/windows/desktop/ms692772) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IViewObjectExImpl Class](../vs140/IViewObjectExImpl-Class.md)   
 [IViewObjectExImpl::SetAdvise](../vs140/IViewObjectExImpl--SetAdvise.md)