---
title: "CDaoTableDef::GetFieldInfo"
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
ms.assetid: c26c2e0f-9a27-40be-a9d3-0c223ebc9c64
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::GetFieldInfo
Call this member function to obtain various kinds of information about a field defined in the tabledef.  
  
## Syntax  
  
```  
  
      void GetFieldInfo(   
   int nIndex,   
   CDaoFieldInfo& fieldinfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
void GetFieldInfo(   
   LPCTSTR lpszName,   
   CDaoFieldInfo& fieldinfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
```  
  
#### Parameters  
 `nIndex`  
 The index of the field object in the table's zero-based Fields collection, for lookup by index.  
  
 `fieldinfo`  
 A reference to a [CDaoFieldInfo](../vs140/CDaoFieldInfo-Structure.md) structure.  
  
 `dwInfoOptions`  
 Options that specify which information about the field to retrieve. The available options are listed here along with what they cause the function to return:  
  
-   `AFX_DAO_PRIMARY_INFO` (Default) Name, Type, Size, Attributes. Use this option for fastest performance.  
  
-   `AFX_DAO_SECONDARY_INFO` Primary information, plus: Ordinal Position, Required, Allow Zero Length, Collating Order, Foreign Name, Source Field, Source Table  
  
-   `AFX_DAO_ALL_INFO` Primary and secondary information, plus: Validation Rule, Validation Text, Default Value  
  
 `lpszName`  
 A pointer to the name of the field object, for lookup by name. The name is a string with up to 64 characters that uniquely names the field.  
  
## Remarks  
 One version of the function lets you look up a field by index. The other version lets you look up a field by name.  
  
 For a description of the information returned, see the [CDaoFieldInfo](../vs140/CDaoFieldInfo-Structure.md) structure. This structure has members that correspond to the items of information listed above in the description of `dwInfoOptions`. When you request information at one level, you get information for any prior levels as well.  
  
 For related information, see the topic "Attributes Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::GetIndexInfo](../vs140/CDaoTableDef--GetIndexInfo.md)   
 [CDaoTableDef::GetIndexCount](../vs140/CDaoTableDef--GetIndexCount.md)   
 [CDaoTableDef::GetFieldCount](../vs140/CDaoTableDef--GetFieldCount.md)