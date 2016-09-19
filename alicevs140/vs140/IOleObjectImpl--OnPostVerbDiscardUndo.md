---
title: "IOleObjectImpl::OnPostVerbDiscardUndo"
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
ms.assetid: d6811945-b7a6-4812-9eb6-18422fb65f3f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPostVerbDiscardUndo
Called by [DoVerbDiscardUndo](../vs140/IOleObjectImpl--DoVerbDiscardUndo.md) after the undo state is discarded.  
  
## Syntax  
  
```  
  
HRESULT OnPostVerbDiscardUndo( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 Override this method with code you want executed after the undo state is discarded.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbDiscardUndo](../vs140/IOleObjectImpl--DoVerbDiscardUndo.md)   
 [IOleObjectImpl::OnPreVerbDiscardUndo](../vs140/IOleObjectImpl--OnPreVerbDiscardUndo.md)