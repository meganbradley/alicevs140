---
title: "IQuickActivateImpl::GetContentExtent"
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
ms.assetid: c1407176-1844-4f97-b367-e0f68126e0e6
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IQuickActivateImpl::GetContentExtent
Retrieves the current display size for a running control.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetContentExtent)(  
   LPSIZEL pSize   
);  
```  
  
## Remarks  
 The size is for a full rendering of the control and is specified in HIMETRIC units.  
  
 See [IQuickActivate::GetContentExtent](http://msdn.microsoft.com/library/windows/desktop/ms693792) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IQuickActivateImpl Class](../vs140/IQuickActivateImpl-Class.md)   
 [IQuickActivateImpl::SetContentExtent](../vs140/IQuickActivateImpl--SetContentExtent.md)