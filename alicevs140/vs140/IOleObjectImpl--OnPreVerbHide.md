---
title: "IOleObjectImpl::OnPreVerbHide"
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
ms.assetid: 5536c2c4-c0c9-4c99-8474-c00db6301519
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPreVerbHide
Called by [DoVerbHide](../vs140/IOleObjectImpl--DoVerbHide.md) before the control is hidden.  
  
## Syntax  
  
```  
  
HRESULT OnPreVerbHide( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 To prevent the control from being hidden, override this method to return an error HRESULT.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbHide](../vs140/IOleObjectImpl--DoVerbHide.md)   
 [IOleObjectImpl::OnPostVerbHide](../vs140/IOleObjectImpl--OnPostVerbHide.md)