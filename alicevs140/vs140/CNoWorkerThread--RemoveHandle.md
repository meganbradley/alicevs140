---
title: "CNoWorkerThread::RemoveHandle"
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
ms.assetid: cd796f00-ab74-4a11-96bc-6952b248c762
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNoWorkerThread::RemoveHandle
Non-functional equivalent of [CWorkerThread::RemoveHandle](../vs140/CWorkerThread--RemoveHandle.md).  
  
## Syntax  
  
```  
  
      HRESULT RemoveHandle(  
   HANDLE /* hObject */   
) throw( );  
```  
  
## Return Value  
 Always returns S_OK.  
  
## Remarks  
 The implementation provided by this class does nothing.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CNoWorkerThread Class](../vs140/CNoWorkerThread-Class.md)