---
title: "IOleObjectImpl::OnPreVerbOpen"
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
ms.assetid: 294aa0cb-176b-4812-9d74-4ef073003704
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPreVerbOpen
Called by [DoVerbOpen](../vs140/IOleObjectImpl--DoVerbOpen.md) before the control has been opened for editing in a separate window.  
  
## Syntax  
  
```  
  
HRESULT OnPreVerbOpen( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 To prevent the control from being opened for editing in a separate window, override this method to return an error HRESULT.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbOpen](../vs140/IOleObjectImpl--DoVerbOpen.md)   
 [IOleObjectImpl::OnPostVerbOpen](../vs140/IOleObjectImpl--OnPostVerbOpen.md)