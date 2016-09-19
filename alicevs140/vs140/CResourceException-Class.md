---
title: "CResourceException Class"
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
ms.assetid: af6ae043-d124-4bfd-b35e-7bb0db67d289
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CResourceException Class
Generated when Windows cannot find or allocate a requested resource.  
  
## Syntax  
  
```  
class CResourceException : public CSimpleException  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CResourceException::CResourceException](#cresourceexception__cresourceexception)|Constructs a `CResourceException` object.|  
  
## Remarks  
 No further qualification is necessary or possible.  
  
 For more information on using `CResourceException`, see the article [Exception Handling (MFC)](../vs140/Exception-Handling-in-MFC.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CException](../vs140/CException-Class.md)  
  
 [CSimpleException](../vs140/CSimpleException-Class.md)  
  
 `CResourceException`  
  
## Requirements  
 **Header:** afxwin.h  
  
##  <a name="cresourceexception__cresourceexception"></a>  CResourceException::CResourceException  
 Constructs a `CResourceException` object.  
  
```  
CResourceException( );  
  
```  
  
### Remarks  
 Do not use this constructor directly, but rather call the global function [AfxThrowResourceException](../vs140/AfxThrowResourceException.md). For more information about exceptions, see the article [Exception Handling (MFC)](../vs140/Exception-Handling-in-MFC.md).  
  
## See Also  
 [Base Class](../vs140/CException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)