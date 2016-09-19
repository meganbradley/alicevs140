---
title: "CDaoQueryDef::Open"
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
ms.assetid: 35518f9d-7927-4ac1-9f90-7043ff81ed28
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::Open
Call this member function to open a querydef previously saved in the database's QueryDefs collection.  
  
## Syntax  
  
```  
  
      virtual void Open(   
   LPCTSTR lpszName = NULL    
);  
```  
  
#### Parameters  
 `lpszName`  
 A string that contains the name of the saved querydef to open. You can use a [CString](../vs140/CStringT-Class.md).  
  
## Remarks  
 Once the querydef is open, you can call its [Execute](../vs140/CDaoQueryDef--Execute.md) member function or use the querydef to create a [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::IsOpen](../vs140/CDaoQueryDef--IsOpen.md)   
 [CDaoQueryDef::Close](../vs140/CDaoQueryDef--Close.md)   
 [CDaoQueryDef::SetName](../vs140/CDaoQueryDef--SetName.md)   
 [CDaoQueryDef::Create](../vs140/CDaoQueryDef--Create.md)