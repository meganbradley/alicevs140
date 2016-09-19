---
title: "CBindStatusCallback::m_spStream"
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
ms.assetid: c3b5a125-ea17-4c4d-8717-27b6f0964682
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::m_spStream
A pointer to the [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) interface of the current bind operation.  
  
## Syntax  
  
```  
  
CComPtr<IStream> m_spStream;  
  
```  
  
## Remarks  
 Initialized in `OnDataAvailable` from the **STGMEDIUM** structure when the **BCSF** flag is **BCSF_FIRSTDATANOTIFICATION** and released when the **BCSF** flag is **BCSF_LASTDATANOTIFICATION**.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::OnDataAvailable](../vs140/CBindStatusCallback--OnDataAvailable.md)   
 [CComPtr Class](../vs140/CComPtr-Class.md)