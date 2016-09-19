---
title: "IViewObjectExImpl::SetAdvise"
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
ms.assetid: dbf1f4ca-2471-4931-8c35-fc1d4cff995d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IViewObjectExImpl::SetAdvise
Sets up a connection between the control and an advise sink so the sink can be notified about changes in the control's view.  
  
## Syntax  
  
```  
  
      STDMETHOD(SetAdvise)(  
   DWORD /* aspects */,  
   DWORD /* advf */,  
   IAdviseSink* pAdvSink   
);  
```  
  
## Remarks  
 The pointer to the [IAdviseSink](http://msdn.microsoft.com/library/windows/desktop/ms692513) interface on the advise sink is stored in the control class data member [CComControlBase::m_spAdviseSink](../vs140/CComControlBase--m_spAdviseSink.md).  
  
 See [IViewObject::SetAdvise](http://msdn.microsoft.com/library/windows/desktop/ms683950) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IViewObjectExImpl Class](../vs140/IViewObjectExImpl-Class.md)   
 [IViewObjectExImpl::GetAdvise](../vs140/IViewObjectExImpl--GetAdvise.md)