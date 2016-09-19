---
title: "IOleObjectImpl::OnPreVerbInPlaceActivate"
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
ms.assetid: 854be84e-85be-4a38-95a9-927d44a3b5f5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPreVerbInPlaceActivate
Called by [DoVerbInPlaceActivate](../vs140/IOleObjectImpl--DoVerbInPlaceActivate.md) before the control is activated in place.  
  
## Syntax  
  
```  
  
HRESULT OnPreVerbInPlaceActivate( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 To prevent the control from being activated in place, override this method to return an error HRESULT.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbInPlaceActivate](../vs140/IOleObjectImpl--DoVerbInPlaceActivate.md)   
 [IOleObjectImpl::OnPostVerbInPlaceActivate](../vs140/IOleObjectImpl--OnPostVerbInPlaceActivate.md)