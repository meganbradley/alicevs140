---
title: "IOleObjectImpl::Unadvise"
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
ms.assetid: fb01b56c-7a81-42e2-8865-d6c8bd8dcf36
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::Unadvise
Deletes the advisory connection stored in the control class's `m_spOleAdviseHolder` data member.  
  
## Syntax  
  
```  
  
      STDMETHOD(Unadvise)(  
   DWORD dwConnection   
);  
```  
  
## Remarks  
 See [IOleObject::Unadvise](http://msdn.microsoft.com/library/windows/desktop/ms693749) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [CComControlBase::m_spOleAdviseHolder](../vs140/CComControlBase--m_spOleAdviseHolder.md)   
 [IOleObjectImpl::Advise](../vs140/IOleObjectImpl--Advise.md)