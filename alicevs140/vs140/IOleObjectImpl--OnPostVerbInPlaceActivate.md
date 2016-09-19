---
title: "IOleObjectImpl::OnPostVerbInPlaceActivate"
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
ms.assetid: d5de547c-80e3-4a28-9501-9e02ac52ea1e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPostVerbInPlaceActivate
Called by [DoVerbInPlaceActivate](../vs140/IOleObjectImpl--DoVerbInPlaceActivate.md) after the control is activated in place.  
  
## Syntax  
  
```  
  
HRESULT OnPostVerbInPlaceActivate( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 Override this method with code you want executed after the control is activated in place.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbInPlaceActivate](../vs140/IOleObjectImpl--DoVerbInPlaceActivate.md)   
 [IOleObjectImpl::OnPreVerbInPlaceActivate](../vs140/IOleObjectImpl--OnPreVerbInPlaceActivate.md)