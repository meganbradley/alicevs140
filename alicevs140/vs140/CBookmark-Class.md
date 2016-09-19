---
title: "CBookmark Class"
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
ms.topic: article
ms.assetid: bc942f95-6f93-41d9-bb6e-bcdae4ae0b7a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBookmark Class
Holds a bookmark value in its buffer.  
  
## Syntax  
  
```  
template < DBLENGTH nSize = 0 >  
class CBookmark : public CBookmarkBase  
template < >  
class CBookmark< 0 > : public CBookmarkBase  
```  
  
#### Parameters  
 `nSize`  
 The size of the bookmark buffer in bytes. When `nSize` is zero, the bookmark buffer will be dynamically created at run time.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[CBookmark](../vs140/CBookmark-Class.md)|The constructor|  
|[GetBuffer](../vs140/CBookmark--GetBuffer.md)|Retrieves the pointer to the buffer.|  
|[GetSize](../vs140/CBookmark--GetSize.md)|Retrieves the size of the buffer in bytes.|  
|[SetBookmark](../vs140/CBookmark--SetBookmark.md)|Sets the bookmark value.|  
  
### Operators  
  
|||  
|-|-|  
|[operator =](../vs140/CBookmark--operator-=.md)|Assigns one `CBookmark` class to another.|  
  
## Remarks  
 **CBookmark<0>** is a template specialization of `CBookmark`; its buffer is dynamically created at run time.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)