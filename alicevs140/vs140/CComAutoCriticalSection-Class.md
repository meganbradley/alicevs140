---
title: "CComAutoCriticalSection Class"
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
ms.assetid: 491a9d90-3398-4f90-88f5-fd2172a46b30
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAutoCriticalSection Class
`CComAutoCriticalSection` provides methods for obtaining and releasing ownership of a critical section object.  
  
## Syntax  
  
```  
  
class CComAutoCriticalSection : public CComCriticalSection  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComAutoCriticalSection::CComAutoCriticalSection](../vs140/CComAutoCriticalSection--CComAutoCriticalSection.md)|The constructor.|  
|[CComAutoCriticalSection::~CComAutoCriticalSection](../vs140/CComAutoCriticalSection--~CComAutoCriticalSection.md)|The destructor.|  
  
## Remarks  
 `CComAutoCriticalSection` is similar to class [CComCriticalSection](../vs140/CComCriticalSection-Class.md), except `CComAutoCriticalSection` automatically initializes the critical section object in the constructor.  
  
 Typically, you use `CComAutoCriticalSection` through the `typedef` name [AutoCriticalSection](../vs140/CComMultiThreadModel--AutoCriticalSection.md). This name references `CComAutoCriticalSection` when [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md) is being used.  
  
 The `Init` and `Term` methods from [CComCriticalSection](../vs140/CComCriticalSection-Class.md) are not available when using this class.  
  
## Inheritance Hierarchy  
 [CComCriticalSection](../vs140/CComCriticalSection-Class.md)  
  
 `CComAutoCriticalSection`  
  
## Requirements  
 **Header:** atlcore.h  
  
##  <a name="ccomautocriticalsection__ccomautocriticalsection"></a>  CComAutoCriticalSection::CComAutoCriticalSection  
 The constructor.  
  
```  
  
CComAutoCriticalSection( );  
  
```  
  
### Remarks  
 Calls the Win32 function [InitializeCriticalSection](http://msdn.microsoft.com/library/windows/desktop/ms683472), which initializes the critical section object.  
  
##  <a name="ccomautocriticalsection___dtorccomautocriticalsection"></a>  CComAutoCriticalSection::~CComAutoCriticalSection  
 The destructor.  
  
```  
  
~CComAutoCriticalSection( ) throw( );  
  
```  
  
### Remarks  
 The destructor calls [DeleteCriticalSection](http://msdn.microsoft.com/library/windows/desktop/ms682552), which releases all system resources used by the critical section object.  
  
## See Also  
 [CComFakeCriticalSection Class](../vs140/CComFakeCriticalSection-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [CComCriticalSection Class](../vs140/CComCriticalSection-Class.md)