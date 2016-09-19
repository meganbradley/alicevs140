---
title: "CDaoDatabase::GetTableDefInfo"
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
ms.assetid: 853a4262-bad6-4cb1-a854-e46f3f44243c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::GetTableDefInfo
Call this member function to obtain various kinds of information about a table defined in the database.  
  
## Syntax  
  
```  
  
      void GetTableDefInfo(   
   int nIndex,   
   CDaoTableDefInfo& tabledefinfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
void GetTableDefInfo(   
   LPCTSTR lpszName,   
   CDaoTableDefInfo& tabledefinfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
```  
  
#### Parameters  
 `nIndex`  
 The index of the tabledef object in the database's TableDefs collection, for lookup by index.  
  
 `tabledefinfo`  
 A reference to a [CDaoTableDefInfo](../vs140/CDaoTableDefInfo-Structure.md) object that returns the information requested.  
  
 `dwInfoOptions`  
 Options that specify which information about the table to retrieve. The available options are listed here along with what they cause the function to return about the relation:  
  
-   `AFX_DAO_PRIMARY_INFO` (Default) Name, Updatable, Attributes  
  
-   `AFX_DAO_SECONDARY_INFO` Primary information plus: Date Created, Date Last Updated, Source Table Name, Connect  
  
-   `AFX_DAO_ALL_INFO` Primary and secondary information plus: Validation Rule, Validation Text, Record Count  
  
 `lpszName`  
 The name of the tabledef object, for lookup by name.  
  
## Remarks  
 Two versions of the function are supplied so you can select a table either by index in the database's TableDefs collection or by the name of the table.  
  
 For a description of the information returned in `tabledefinfo`, see the [CDaoTableDefInfo](../vs140/CDaoTableDefInfo-Structure.md) structure. This structure has members that correspond to the items of information listed above in the description of `dwInfoOptions`. If you request information at one level, you get information for any prior levels as well.  
  
> [!NOTE]
>  The `AFX_DAO_ALL_INFO` option provides information that can be slow to obtain. In this case, counting the records in the table could be very time consuming if there are many records.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoDatabase::GetTableDefCount](../vs140/CDaoDatabase--GetTableDefCount.md)