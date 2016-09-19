---
title: "IOleObjectImpl::OnPostVerbHide"
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
ms.assetid: b866d1a6-597b-4321-bc7c-24bd7993766c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPostVerbHide
Called by [DoVerbHide](../vs140/IOleObjectImpl--DoVerbHide.md) after the control is hidden.  
  
## Syntax  
  
```  
  
HRESULT OnPostVerbHide( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 Override this method with code you want executed after the control is hidden.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbHide](../vs140/IOleObjectImpl--DoVerbHide.md)   
 [IOleObjectImpl::OnPreVerbHide](../vs140/IOleObjectImpl--OnPreVerbHide.md)