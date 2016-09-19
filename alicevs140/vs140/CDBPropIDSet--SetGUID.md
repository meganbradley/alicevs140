---
title: "CDBPropIDSet::SetGUID"
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
ms.assetid: 8dd0f3bf-1490-4d53-9063-322b8d821bbe
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDBPropIDSet::SetGUID
Sets the GUID field in the **DBPROPIDSET** structure.  
  
## Syntax  
  
```  
  
      void SetGUID(   
   const GUID& guid    
) throw( );  
```  
  
#### Parameters  
 `guid`  
 [in] A GUID used to set the **guidPropertySet** field of the [DBPROPIDSET](https://msdn.microsoft.com/en-us/library/ms717981.aspx) structure.  
  
## Remarks  
 This field can be set by the [constructor](../vs140/CDBPropIDSet--CDBPropIDSet.md) as well. Call this function if you use the default constructor for this class.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDBPropIDSet Class](../vs140/CDBPropIDSet-Class.md)