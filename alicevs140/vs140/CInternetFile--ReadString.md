---
title: "CInternetFile::ReadString"
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
ms.assetid: 8f1dedf2-2596-4ea5-9d5a-775475f106ea
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetFile::ReadString
Call this member function to read a stream of characters until it finds a newline character.  
  
## Syntax  
  
```  
  
      virtual BOOL ReadString(   
   CString& rString    
);  
virtual LPTSTR ReadString(   
   LPTSTR pstr,   
   UINT nMax    
);  
```  
  
#### Parameters  
 `pstr`  
 A pointer to a string which will receive the line being read.  
  
 `nMax`  
 The maximum number of characters to be read.  
  
 `rString`  
 A reference to the [CString](../vs140/CStringT-Class.md) object that receives the read line.  
  
## Return Value  
 A pointer to the buffer containing plain data retrieved from the [CInternetFile](../vs140/CInternetFile-Class.md) object. Regardless of the data type of the buffer passed to this method, it does not perform any manipulations on the data (for example, conversion to Unicode), so you must map the returned data to the structure you expect, as if the **void\*** type were returned.  
  
 **NULL** if end-of-file was reached without reading any data; or, if boolean, **FALSE** if end-of-file was reached without reading any data.  
  
## Remarks  
 The function places the resulting line into the memory referenced by the `pstr` parameter. It stops reading characters when it reaches the maximum number of characters, specified by `nMax`. The buffer always receives a terminating null character.  
  
 If you call `ReadString` without first calling [SetReadBufferSize](../vs140/CInternetFile--SetReadBufferSize.md), you will get a buffer of 4096 bytes.  
  
## Exceptions  
 This method can throw exceptions of type `CInternetException*`.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetFile Class](../vs140/CInternetFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)