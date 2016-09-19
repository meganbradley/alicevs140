---
title: "CDaoQueryDef::GetParameterInfo"
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
ms.assetid: 7615505f-2fb0-43c7-8ebf-7f12b22735a2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetParameterInfo
Call this member function to obtain information about a parameter defined in the querydef.  
  
## Syntax  
  
```  
  
      void GetParameterInfo(   
   int nIndex,   
   CDaoParameterInfo& paraminfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
void GetParameterInfo(   
   LPCTSTR lpszName,   
   CDaoParameterInfo& paraminfo,   
   DWORD dwInfoOptions = AFX_DAO_PRIMARY_INFO    
);  
```  
  
#### Parameters  
 `nIndex`  
 The zero-based index of the desired parameter in the querydef's Parameters collection, for lookup by index.  
  
 `paraminfo`  
 A reference to a [CDaoParameterInfo](../vs140/CDaoParameterInfo-Structure.md) object that returns the information requested.  
  
 `dwInfoOptions`  
 Options that specify which information about the parameter to retrieve. The available option is listed here along with what it causes the function to return:  
  
-   `AFX_DAO_PRIMARY_INFO` (Default) Name, Type  
  
 `lpszName`  
 A string containing the name of the desired parameter, for lookup by name. You can use a [CString](../vs140/CStringT-Class.md).  
  
## Remarks  
 For a description of the information returned in `paraminfo`, see the [CDaoParameterInfo](../vs140/CDaoParameterInfo-Structure.md) structure. This structure has members that correspond to the descriptive information under `dwInfoOptions` above.  
  
 For related information, see the topic "PARAMETERS Declaration (SQL)" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::GetParameterCount](../vs140/CDaoQueryDef--GetParameterCount.md)