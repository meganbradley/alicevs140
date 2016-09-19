---
title: "CComHeapPtr::CComHeapPtr"
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
ms.assetid: 7468b740-9a87-4cb6-860a-012428854166
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComHeapPtr::CComHeapPtr
The constructor.  
  
## Syntax  
  
```  
  
      CComHeapPtr( ) throw( );   
explicit CComHeapPtr(  
   T* pData   
) throw( );  
```  
  
#### Parameters  
 `pData`  
 An existing `CComHeapPtr` object.  
  
## Remarks  
 The heap pointer can optionally be created using an existing `CComHeapPtr` object. If so, the new `CComHeapPtr` object assumes responsibility for managing the new pointer and resources.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComHeapPtr Class](../vs140/CComHeapPtr-Class.md)