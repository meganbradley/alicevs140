---
title: "CInternetFile::Write"
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
ms.assetid: 021ef57e-a7db-400c-8ddb-eaa0b2e6ca47
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetFile::Write
Call this member function to write into the given memory, `lpvBuf`, the specified number of bytes, `nCount`.  
  
## Syntax  
  
```  
  
      virtual void Write(   
   const void* lpBuf,   
   UINT nCount    
);  
```  
  
#### Parameters  
 `lpBuf`  
 A pointer to the first byte to be written.  
  
 `nCount`  
 Specifies the number of bytes to be written.  
  
## Remarks  
 If any error occurs while writing the data, the function throws a [CInternetException](../vs140/CInternetException-Class.md) object describing the error.  
  
## Exceptions  
 This method can throw exceptions of type `CInternetException`.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetFile Class](../vs140/CInternetFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)