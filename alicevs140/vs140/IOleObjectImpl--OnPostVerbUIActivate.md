---
title: "IOleObjectImpl::OnPostVerbUIActivate"
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
ms.assetid: baab8f7c-2afd-472b-8076-80275b618af4
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPostVerbUIActivate
Called by [DoVerbUIActivate](../vs140/IOleObjectImpl--DoVerbUIActivate.md) after the control's user interface has been activated.  
  
## Syntax  
  
```  
  
HRESULT OnPostVerbUIActivate( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 Override this method with code you want executed after the control's user interface has been activated.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbUIActivate](../vs140/IOleObjectImpl--DoVerbUIActivate.md)   
 [IOleObjectImpl::OnPreVerbUIActivate](../vs140/IOleObjectImpl--OnPreVerbUIActivate.md)