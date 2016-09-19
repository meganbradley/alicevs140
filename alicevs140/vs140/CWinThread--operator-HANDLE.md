---
title: "CWinThread::operator HANDLE"
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
ms.assetid: 083f2fb3-4353-4ed5-8dee-cdb659b0b0b2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::operator HANDLE
Retrieves the handle of the `CWinThread` object.  
  
## Syntax  
  
```  
  
operator HANDLE( ) const;  
  
```  
  
## Return Value  
 If successful, the handle of the thread object; otherwise, **NULL**.  
  
## Remarks  
 Use the handle to directly call Windows APIs.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)