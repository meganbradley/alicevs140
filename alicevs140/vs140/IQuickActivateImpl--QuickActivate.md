---
title: "IQuickActivateImpl::QuickActivate"
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
ms.assetid: ea4af25a-8b19-4610-baa2-cff975931279
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IQuickActivateImpl::QuickActivate
Performs quick initialization of controls being loaded.  
  
## Syntax  
  
```  
  
      STDMETHOD(QuickActivate)(  
   QACONTAINER* pQACont,  
   QACONTROL* pQACtrl   
);  
```  
  
## Remarks  
 The structure contains pointers to interfaces needed by the control and the values of some ambient properties. Upon return, the control passes a pointer to a [QACONTROL](http://msdn.microsoft.com/library/windows/desktop/ms693721) structure that contains pointers to its own interfaces that the container requires, and additional status information.  
  
 See [IQuickActivate::QuickActivate](http://msdn.microsoft.com/library/windows/desktop/ms682421) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IQuickActivateImpl Class](../vs140/IQuickActivateImpl-Class.md)