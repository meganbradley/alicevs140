---
title: "CDaoQueryDef::GetFieldInfo"
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
ms.assetid: f1fa4b04-d2f4-4c16-96a1-81838db9f231
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetFieldInfo
Call this member function to obtain various kinds of information about a field defined in the querydef.  
  
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
 The zero-based index of the desired field in the querydef's Fields collection, for lookup by index.  
  
 `fieldinfo`  
 A reference to a `CDaoFieldInfo` object that returns the information requested.  
  
 `dwInfoOptions`  
 Options that specify which information about the field to retrieve. The available options are listed here along with what they cause the function to return:  
  
-   `AFX_DAO_PRIMARY_INFO` (Default) Name, Type, Size, Attributes  
  
-   `AFX_DAO_SECONDARY_INFO` Primary information plus: Ordinal Position, Required, Allow Zero Length, Source Field, Foreign Name, Source Table, Collating Order  
  
-   `AFX_DAO_ALL_INFO` Primary and secondary information plus: Default Value, Validation Text, Validation Rule  
  
 `lpszName`  
 A string containing the name of the desired field, for lookup by name. You can use a [CString](../vs140/CStringT-Class.md).  
  
## Remarks  
 For a description of the information returned in `fieldinfo`, see the [CDaoFieldInfo](../vs140/CDaoFieldInfo-Structure.md) structure. This structure has members that correspond to the descriptive information under `dwInfoOptions` above. If you request one level of information, you get any prior levels of information as well.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::GetFieldCount](../vs140/CDaoQueryDef--GetFieldCount.md)