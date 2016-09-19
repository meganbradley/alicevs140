---
title: "CDaoDatabase::GetRelationInfo"
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
ms.assetid: 1f6d432a-a827-46b1-b5ce-c11601849760
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::GetRelationInfo
Call this member function to obtain information about a specified relation in the database's Relations collection.  
  
## Syntax  
  
```  
  
      void GetRelationInfo(   
   int nIndex,   
   CDaoRelationInfo& relinfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
void GetRelationInfo(   
   LPCTSTR lpszName,   
   CDaoRelationInfo& relinfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
```  
  
#### Parameters  
 `nIndex`  
 The index of the relation object in the database's Relations collection, for lookup by index.  
  
 *relinfo*  
 A reference to a [CDaoRelationInfo](../vs140/CDaoRelationInfo-Structure.md) object that returns the information requested.  
  
 `dwInfoOptions`  
 Options that specify which information about the relation to retrieve. The available options are listed here along with what they cause the function to return about the relation:  
  
-   `AFX_DAO_PRIMARY_INFO` (Default) Name, Table, Foreign Table  
  
-   `AFX_DAO_SECONDARY_INFO` Attributes, Field Information  
  
 The Field Information is a [CDaoRelationFieldInfo](../vs140/CDaoRelationFieldInfo-Structure.md) object containing the fields from the primary table involved in the relation.  
  
 `lpszName`  
 A string containing the name of the relation object, for lookup by name.  
  
## Remarks  
 Two versions of this function provide access either by index or by name. For a description of the information returned in *relinfo*, see the [CDaoRelationInfo](../vs140/CDaoRelationInfo-Structure.md) structure. This structure has members that correspond to the items of information listed above in the description of `dwInfoOptions`. If you request information at one level, you also get information at any prior levels as well.  
  
> [!NOTE]
>  If you set the relation object's attributes to activate cascade operations (**dbRelationUpdateCascades** or **dbRelationDeleteCascades**), the Microsoft Jet database engine automatically updates or deletes records in one or more other tables when changes are made to related primary key tables. For example, suppose you establish a cascade delete relationship between a Customers table and an Orders table. When you delete records from the Customers table, records in the Orders table related to that customer are also deleted. In addition, if you establish cascade delete relationships between the Orders table and other tables, records from those tables are automatically deleted when you delete records from the Customers table.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoDatabase::GetRelationCount](../vs140/CDaoDatabase--GetRelationCount.md)