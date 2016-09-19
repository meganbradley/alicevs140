---
title: "CInternetException Class"
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
ms.assetid: 44fb3cbe-523e-4754-8843-a77909990b14
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetException Class
Represents an exception condition related to an Internet operation.  
  
## Syntax  
  
```  
class CInternetException : public CException  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CInternetException::CInternetException](#cinternetexception__cinternetexception)|Constructs a `CInternetException` object.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CInternetException::m_dwContext](#cinternetexception__m_dwcontext)|The context value associated with the operation that caused the exception.|  
|[CInternetException::m_dwError](#cinternetexception__m_dwerror)|The error that caused the exception.|  
  
## Remarks  
 The `CInternetException` class includes two public data members: one holds the error code associated with the exception, and the other holds the context identifier of the Internet application associated with the error.  
  
 For more information about context identifiers for Internet applications, see the article [Internet Programming with WinInet](../vs140/Win32-Internet-Extensions--WinInet-.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CException](../vs140/CException-Class.md)  
  
 `CInternetException`  
  
## Requirements  
 **Header:** afxinet.h  
  
##  <a name="cinternetexception__cinternetexception"></a>  CInternetException::CInternetException  
 This member function is called when a `CInternetException` object is created.  
  
```  
CInternetException(    DWORD  dwError );  
  
```  
  
### Parameters  
 `dwError`  
 The error that caused the exception.  
  
### Remarks  
 To throw a CInternetException, call the MFC global function [AfxThrowInternetException](../vs140/AfxThrowInternetException.md).  
  
##  <a name="cinternetexception__m_dwcontext"></a>  CInternetException::m_dwContext  
 The context value associated with the related Internet operation.  
  
```  
DWORD_PTR m_dwContext;  
  
```  
  
### Remarks  
 The context identifier is originally specified in [CInternetSession](../vs140/CInternetSession-Class.md) and passed by MFC to [CInternetConnection](../vs140/CInternetConnection-Class.md)- and [CInternetFile](../vs140/CInternetFile-Class.md)-derived classes. You can override this default and assign any `dwContext` parameter a value of your choosing. `dwContext` is associated with any operation of the given object. `dwContext` identifies the operation's status information returned by [CInternetSession::OnStatusCallback](../vs140/CInternetSession-Class.md#cinternetsession__onstatuscallback).  
  
##  <a name="cinternetexception__m_dwerror"></a>  CInternetException::m_dwError  
 The error that caused the exception.  
  
```  
DWORD m_dwError;  
  
```  
  
### Remarks  
 This error value may be a system error code, found in WINERROR.H, or an error value from WININET.H.  
  
 For a list of Win32 error codes, see                         [Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms681381). For a list of Internet-specific error messages, see  . Both topics are in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [Base Class](../vs140/CException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CException](../vs140/CException-Class.md)