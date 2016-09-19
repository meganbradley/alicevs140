---
title: "CGopherConnection::GetAttribute"
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
ms.assetid: e22acbd4-ce0f-4c6e-9fe7-ce61dda130a8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherConnection::GetAttribute
Call this member function to retrieve specific attribute information about an item from the gopher server.  
  
## Syntax  
  
```  
  
      BOOL GetAttribute(  
   CGopherLocator& refLocator  
   CString strRequestedAttributes,  
   CString& strResult,  
);  
```  
  
#### Parameters  
 `refLocator`  
 A reference to a [CGopherLocator](../vs140/CGopherLocator-Class.md) object.  
  
 *strRequestedAttributes*  
 A space-delimited string specifying the names of the requested attributes.  
  
 `strResult`  
 A reference to a [CString](../vs140/CStringT-Class.md) that receives the locator type.  
  
## Return Value  
 Nonzero if successful; otherwise 0. If the call fails, the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) may be called to determine the cause of the error.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CGopherConnection Class](../vs140/CGopherConnection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [CHttpConnection Class](../vs140/CHttpConnection-Class.md)   
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)   
 [CGopherLocator Class](../vs140/CGopherLocator-Class.md)