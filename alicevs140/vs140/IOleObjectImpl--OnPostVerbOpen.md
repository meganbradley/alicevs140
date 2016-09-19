---
title: "IOleObjectImpl::OnPostVerbOpen"
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
ms.assetid: 5a1e5a83-0b62-4808-96f9-1a59ec9eea0a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPostVerbOpen
Called by [DoVerbOpen](../vs140/IOleObjectImpl--DoVerbOpen.md) after the control has been opened for editing in a separate window.  
  
## Syntax  
  
```  
  
HRESULT OnPostVerbOpen( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 Override this method with code you want executed after the control has been opened for editing in a separate window.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbOpen](../vs140/IOleObjectImpl--DoVerbOpen.md)   
 [IOleObjectImpl::OnPreVerbOpen](../vs140/IOleObjectImpl--OnPreVerbOpen.md)