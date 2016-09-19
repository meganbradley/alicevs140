---
title: "CDaoDatabase::GetQueryDefInfo"
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
ms.assetid: 9994cfcb-e610-47e4-bf78-8f83263e21c6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::GetQueryDefInfo
Call this member function to obtain various kinds of information about a query defined in the database.  
  
## Syntax  
  
```  
  
      void GetQueryDefInfo(   
   int nIndex,   
   CDaoQueryDefInfo& querydefinfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
void GetQueryDefInfo(   
   LPCTSTR lpszName,   
   CDaoQueryDefInfo& querydefinfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
```  
  
#### Parameters  
 `nIndex`  
 The index of the predefined query in the database's QueryDefs collection, for lookup by index.  
  
 *querydefinfo*  
 A reference to a [CDaoQueryDefInfo](../vs140/CDaoQueryDefInfo-Structure.md) object that returns the information requested.  
  
 `dwInfoOptions`  
 Options that specify which information about the recordset to retrieve. The available options are listed here along with what they cause the function to return about the recordset:  
  
-   `AFX_DAO_PRIMARY_INFO` (Default) Name, Type  
  
-   `AFX_DAO_SECONDARY_INFO` Primary information plus: Date Created, Date of Last Update, Returns Records, Updatable  
  
-   `AFX_DAO_ALL_INFO` Primary and secondary information plus: SQL, Connect, ODBCTimeout  
  
 `lpszName`  
 A string containing the name of a query defined in the database, for lookup by name.  
  
## Remarks  
 Two versions of the function are supplied so you can select a query either by index in the database's QueryDefs collection or by the name of the query.  
  
 For a description of the information returned in *querydefinfo*, see the [CDaoQueryDefInfo](../vs140/CDaoQueryDefInfo-Structure.md) structure. This structure has members that correspond to the items of information listed above in the description of `dwInfoOptions`. If you request one level of information, you get any prior levels of information as well.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoDatabase::GetQueryDefCount](../vs140/CDaoDatabase--GetQueryDefCount.md)