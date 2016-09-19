---
title: "CHttpFile::GetFileURL"
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
ms.assetid: 447c57da-881d-4e04-90d0-ac7335ae831c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHttpFile::GetFileURL
Call this member function to get the name of the HTTP file as a URL.  
  
## Syntax  
  
```  
  
virtual CString GetFileURL( ) const;  
  
```  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) object containing a URL referencing the resource associated with this file.  
  
## Remarks  
 Use this member function only after a successful call to [SendRequest](../vs140/CHttpFile--SendRequest.md) or on a `CHttpFile` object successfully created by [OpenURL](../vs140/CInternetSession--OpenURL.md).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CHttpFile Class](../vs140/CHttpFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetFile Class](../vs140/CInternetFile-Class.md)