---
title: "CAtlException Class"
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
ms.assetid: 3fd7b041-f70d-4292-b947-0d70781d95a8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlException Class
This class defines an ATL exception.  
  
## Syntax  
  
```  
  
class CAtlException  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlException::CAtlException](../vs140/CAtlException--CAtlException.md)|The constructor.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlException::operator HRESULT](../vs140/CAtlException--operator-HRESULT.md)|Casts the current object to an HRESULT value.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlException::m_hr](../vs140/CAtlException--m_hr.md)|The variable of type HRESULT created by the object and used to store the error condition.|  
  
## Remarks  
 A `CAtlException` object represents an exception condition related to an ATL operation. The `CAtlException` class includes a public data member that stores the status code indicating the reason for the exception and a cast operator that allows you to treat the exception as if it were an HRESULT.  
  
 In general, you will call `AtlThrow` rather than creating a `CAtlException` object directly.  
  
## Requirements  
 **Header:** atlexcept.h  
  
##  <a name="catlexception__catlexception"></a>  CAtlException::CAtlException  
 The constructor.  
  
```  
  
CAtlException(  
      HRESULT  hr  
   ) throw( );  
   CAtlException( ) throw( );  
  
```  
  
### Parameters  
 `hr`  
 The `HRESULT` error code.  
  
##  <a name="catlexception__operator_hresult"></a>  CAtlException::operator HRESULT  
 Casts the current object to an HRESULT value.  
  
```  
  
operator HRESULT( ) const throw ( );  
  
```  
  
##  <a name="catlexception__m_hr"></a>  CAtlException::m_hr  
 The `HRESULT` data member.  
  
```  
  
HRESULT m_hr;  
  
```  
  
### Remarks  
 The data member that stores the error condition. The HRESULT value is set by the constructor, [CAtlException::CAtlException](../vs140/CAtlException--CAtlException.md).  
  
## See Also  
 [AtlThrow](../vs140/AtlThrow.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)