---
title: "IOleObjectImpl::OnPreVerbUIActivate"
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
ms.assetid: 3cb9755f-9f05-4f7a-9edf-f3601f01d3a5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPreVerbUIActivate
Called by [DoVerbUIActivate](../vs140/IOleObjectImpl--DoVerbUIActivate.md) before the control's user interface has been activated.  
  
## Syntax  
  
```  
  
HRESULT OnPreVerbUIActivate( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 To prevent the control's user interface from being activated, override this method to return an error HRESULT.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbUIActivate](../vs140/IOleObjectImpl--DoVerbUIActivate.md)   
 [IOleObjectImpl::OnPostVerbUIActivate](../vs140/IOleObjectImpl--OnPostVerbUIActivate.md)