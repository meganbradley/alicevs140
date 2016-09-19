---
title: "CDataSource::GetProperty"
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
ms.assetid: 6531147c-b164-4ab5-a4a7-509634b85b4d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataSource::GetProperty
Returns the value of a specified property for the connected data source object.  
  
## Syntax  
  
```  
  
      HRESULT GetProperty(   
   const GUID& guid,   
   DBPROPID propid,   
   VARIANT* pVariant    
) const throw( );  
```  
  
#### Parameters  
 `guid`  
 [in] A GUID identifying the property set for which to return the property.  
  
 `propid`  
 [in] Property ID for the property to return.  
  
 *pVariant*  
 [out] A pointer to the variant where **GetProperty** returns the value of the property.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 To get multiple properties, use [GetProperties](../vs140/CDataSource--GetProperties.md).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDataSource Class](../vs140/CDataSource-Class.md)