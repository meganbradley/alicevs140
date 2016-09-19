---
title: "CComAutoThreadModule::Init"
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
ms.assetid: c4471fcd-34db-4ec4-a2bd-d8605e98307f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAutoThreadModule::Init
As of ATL 7.0, `CComAutoThreadModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
      HRESULT Init(  
   _ATL_OBJMAP_ENTRY* p,  
   HINSTANCE h,  
   const GUID* plibid = NULL,  
   int nThreads = GetDefaultThreads( )  
);  
```  
  
#### Parameters  
 `p`  
 [in] A pointer to an array of object map entries.  
  
 `h`  
 [in] The `HINSTANCE` passed to **DLLMain** or `WinMain`.  
  
 `plibid`  
 [in] A pointer to the LIBID of the type library associated with the project.  
  
 `nThreads`  
 [in] The number of threads to be created. By default, `nThreads` is the value returned by [GetDefaultThreads](../vs140/CComAutoThreadModule--GetDefaultThreads.md).  
  
## Remarks  
 Initializes data members and creates the number of threads specified by `nThreads`.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComAutoThreadModule Class](../vs140/CComAutoThreadModule-Class.md)   
 [CComAutoThreadModule::m_nThreads](../vs140/CComAutoThreadModule--m_nThreads.md)