---
title: "IOleObjectImpl::OnPostVerbShow"
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
ms.assetid: 37311c36-5975-4679-aabe-798c22ce9e89
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPostVerbShow
Called by [DoVerbShow](../vs140/IOleObjectImpl--DoVerbShow.md) after the control has been made visible.  
  
## Syntax  
  
```  
  
HRESULT OnPostVerbShow( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 Override this method with code you want executed after the control has been made visible.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbShow](../vs140/IOleObjectImpl--DoVerbShow.md)   
 [IOleObjectImpl::OnPreVerbShow](../vs140/IOleObjectImpl--OnPreVerbShow.md)