---
title: "CAutoPtr::~CAutoPtr"
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
ms.assetid: e7c0da08-5f29-436c-9b06-63d83c744601
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoPtr::~CAutoPtr
The destructor.  
  
## Syntax  
  
```  
  
~CAutoPtr( ) throw( );  
  
```  
  
## Remarks  
 Frees any allocated resources. Calls [CAutoPtr::Free](../vs140/CAutoPtr--Free.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoPtr Class](../vs140/CAutoPtr-Class.md)   
 [CAutoPtr::CAutoPtr](../vs140/CAutoPtr--CAutoPtr.md)