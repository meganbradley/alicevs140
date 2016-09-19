---
title: "CGopherFileFind::CGopherFileFind"
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
ms.assetid: cd99d01b-eee6-449d-8c89-770cce7f318b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherFileFind::CGopherFileFind
This member function is called to construct a `CGopherFileFind` object.  
  
## Syntax  
  
```  
  
      explicit CGopherFileFind(  
   CGopherConnection* pConnection,  
   DWORD_PTR dwContext = 1   
);  
```  
  
#### Parameters  
 `pConnection`  
 A pointer to a [CGopherConnection](../vs140/CGopherConnection-Class.md) object.  
  
 `dwContext`  
 The context identifier for the operation. See **Remarks** for more information about `dwContext`.  
  
## Remarks  
 The default value for `dwContext` is sent by MFC to the `CGopherFileFind` object from the [CInternetSession](../vs140/CInternetSession-Class.md) object that created the `CGopherFileFind` object. When you construct a `CGopherFileFind` object, you can override the default to set the context identifier to a value of your choosing. The context identifier is returned to [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md) to provide status on the object with which it is identified. See the article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md) for more information about the context identifier.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CGopherFileFind Class](../vs140/CGopherFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFtpFileFind Class](../vs140/CFtpFileFind-Class.md)   
 [CFileFind Class](../vs140/CFileFind-Class.md)