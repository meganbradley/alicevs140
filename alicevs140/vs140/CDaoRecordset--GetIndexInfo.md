---
title: "CDaoRecordset::GetIndexInfo"
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
ms.assetid: b6ea9b44-5255-4887-bfa2-08829e4848aa
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetIndexInfo
Call this member function to obtain various kinds of information about an index defined in the base table underlying a recordset.  
  
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
 The zero-based index in the table's Indexes collection, for lookup by numerical position.  
  
 `indexinfo`  
 A reference to a [CDaoIndexInfo](../vs140/CDaoIndexInfo-Structure.md) structure.  
  
 `dwInfoOptions`  
 Options that specify which information about the index to retrieve. The available options are listed here along with what they cause the function to return. For best performance, retrieve only the level of information you need:  
  
-   `AFX_DAO_PRIMARY_INFO` (Default) Name, Field Info, Fields  
  
-   `AFX_DAO_SECONDARY_INFO` Primary information, plus: Primary, Unique, Clustered, IgnoreNulls, Required, Foreign  
  
-   `AFX_DAO_ALL_INFO` Primary and secondary information, plus: Distinct Count  
  
 `lpszName`  
 A pointer to the name of the index object, for lookup by name.  
  
## Remarks  
 One version of the function lets you look up a index by its position in the collection. The other version lets you look up an index by name.  
  
 For a description of the information returned, see the [CDaoIndexInfo](../vs140/CDaoIndexInfo-Structure.md) structure. This structure has members that correspond to the items of information listed above in the description of `dwInfoOptions`. When you request information at one level, you get information for any prior levels as well.  
  
 For related information, see the topic "Attributes Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetFieldCount](../vs140/CDaoRecordset--GetFieldCount.md)   
 [CDaoRecordset::GetFieldInfo](../vs140/CDaoRecordset--GetFieldInfo.md)   
 [CDaoRecordset::GetIndexCount](../vs140/CDaoRecordset--GetIndexCount.md)   
 [CDaoRecordset::GetLastModifiedBookmark](../vs140/CDaoRecordset--GetLastModifiedBookmark.md)