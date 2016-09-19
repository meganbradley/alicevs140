---
title: "IOleObjectImpl::Advise"
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
ms.assetid: 1ec2fb1a-741e-4cca-8eb7-cd7e322102cd
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::Advise
Establishes an advisory connection with the control.  
  
## Syntax  
  
```  
  
      STDMETHOD(Advise)(  
   IAdviseSink* pAdvSink,  
   DWORD* pdwConnection   
);  
```  
  
## Remarks  
 See [IOleObject::Advise](http://msdn.microsoft.com/library/windows/desktop/ms686573) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [CComControlBase::m_spOleAdviseHolder](../vs140/CComControlBase--m_spOleAdviseHolder.md)   
 [IOleObjectImpl::Unadvise](../vs140/IOleObjectImpl--Unadvise.md)