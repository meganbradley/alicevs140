---
title: "CInternetException::CInternetException"
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
ms.assetid: 1bc9a6a8-9b64-4be4-a608-c64792145945
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetException::CInternetException
This member function is called when a `CInternetException` object is created.  
  
## Syntax  
  
```  
  
      CInternetException(  
   DWORD dwError   
);  
```  
  
#### Parameters  
 `dwError`  
 The error that caused the exception.  
  
## Remarks  
 To throw a CInternetException, call the MFC global function [AfxThrowInternetException](../vs140/AfxThrowInternetException.md).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetException Class](../vs140/CInternetException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CException Class](../vs140/CException-Class.md)