---
title: "CNotSupportedException Class"
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
ms.assetid: e517391b-eb94-4c39-ae32-87b45bf7d624
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNotSupportedException Class
Represents an exception that is the result of a request for an unsupported feature.  
  
## Syntax  
  
```  
class CNotSupportedException : public CSimpleException  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CNotSupportedException::CNotSupportedException](#cnotsupportedexception__cnotsupportedexception)|Constructs a `CNotSupportedException` object.|  
  
## Remarks  
 No further qualification is necessary or possible.  
  
 For more information on using `CNotSupportedException`, see the article [Exception Handling (MFC)](../vs140/Exception-Handling-in-MFC.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CException](../vs140/CException-Class.md)  
  
 [CSimpleException](../vs140/CSimpleException-Class.md)  
  
 `CNotSupportedException`  
  
## Requirements  
 **Header:** afx.h  
  
##  <a name="cnotsupportedexception__cnotsupportedexception"></a>  CNotSupportedException::CNotSupportedException  
 Constructs a `CNotSupportedException` object.  
  
```  
CNotSupportedException( );  
  
```  
  
### Remarks  
 Do not use this constructor directly, but rather call the global function [AfxThrowNotSupportedException](../vs140/AfxThrowNotSupportedException.md). For more information about exception processing, see the article [Exceptions](../vs140/Exception-Handling-in-MFC.md).  
  
## See Also  
 [Base Class](../vs140/CException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)