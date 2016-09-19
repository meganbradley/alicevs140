---
title: "IQuickActivateImpl::SetContentExtent"
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
ms.assetid: 426c976a-fb49-4c9c-b389-bd4c29b40f5b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IQuickActivateImpl::SetContentExtent
Informs the control of how much display space the container has assigned to it.  
  
## Syntax  
  
```  
  
      STDMETHOD(SetContentExtent)(  
   LPSIZEL pSize   
);  
```  
  
## Remarks  
 The size is specified in HIMETRIC units.  
  
 See [IQuickActivate::SetContentExtent](http://msdn.microsoft.com/library/windows/desktop/ms678806) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IQuickActivateImpl Class](../vs140/IQuickActivateImpl-Class.md)   
 [IQuickActivateImpl::GetContentExtent](../vs140/IQuickActivateImpl--GetContentExtent.md)