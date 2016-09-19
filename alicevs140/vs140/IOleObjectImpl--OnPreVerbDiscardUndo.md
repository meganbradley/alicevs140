---
title: "IOleObjectImpl::OnPreVerbDiscardUndo"
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
ms.assetid: 53e6fa48-c156-4b60-82b7-6781c31c4808
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::OnPreVerbDiscardUndo
Called by [DoVerbDiscardUndo](../vs140/IOleObjectImpl--DoVerbDiscardUndo.md) before the undo state is discarded.  
  
## Syntax  
  
```  
  
HRESULT OnPreVerbDiscardUndo( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 To prevent the undo state from being discarded, override this method to return an error HRESULT.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbDiscardUndo](../vs140/IOleObjectImpl--DoVerbDiscardUndo.md)   
 [IOleObjectImpl::OnPostVerbDiscardUndo](../vs140/IOleObjectImpl--OnPostVerbDiscardUndo.md)