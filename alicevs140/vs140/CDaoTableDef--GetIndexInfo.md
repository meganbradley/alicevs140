---
title: "CDaoTableDef::GetIndexInfo"
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
ms.assetid: 1acbd84d-dd73-44cc-945d-dac38a820621
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::GetIndexInfo
Call this member function to obtain various kinds of information about an index defined in the tabledef.  
  
## Syntax  
  
```  
  
      void GetIndexInfo(   
   int nIndex,   
   CDaoIndexInfo& indexinfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
void GetIndexInfo(   
   LPCTSTR lpszName,   
   CDaoIndexInfo& indexinfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
```  
  
#### Parameters  
 `nIndex`  
 The numeric index of the Index object in the table's zero-based Indexes collection, for lookup by its position in the collection.  
  
 `indexinfo`  
 A reference to a [CDaoIndexInfo](../vs140/CDaoIndexInfo-Structure.md) structure.  
  
 `dwInfoOptions`  
 Options that specify which information about the index to retrieve. The available options are listed here along with what they cause the function to return:  
  
-   `AFX_DAO_PRIMARY_INFO` Name, Field Info, Fields. Use this option for fastest performance.  
  
-   `AFX_DAO_SECONDARY_INFO` Primary information, plus: Primary, Unique, Clustered, Ignore Nulls, Required, Foreign  
  
-   `AFX_DAO_ALL_INFO` Primary and secondary information, plus: Distinct Count  
  
 `lpszName`  
 A pointer to the name of the index object, for lookup by name.  
  
## Remarks  
 One version of the function lets you look up an index by its position in the collection. The other version lets you look up an index by name.  
  
 For a description of the information returned, see the [CDaoIndexInfo](../vs140/CDaoIndexInfo-Structure.md) structure. This structure has members that correspond to the items of information listed above in the description of `dwInfoOptions`. When you request information at one level, you get information for any prior levels as well.  
  
 For related information, see the topic "Attributes Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::GetFieldInfo](../vs140/CDaoTableDef--GetFieldInfo.md)   
 [CDaoTableDef::GetIndexCount](../vs140/CDaoTableDef--GetIndexCount.md)   
 [CDaoTableDef::GetFieldCount](../vs140/CDaoTableDef--GetFieldCount.md)