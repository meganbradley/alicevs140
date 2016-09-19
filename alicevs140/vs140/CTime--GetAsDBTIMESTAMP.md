---
title: "CTime::GetAsDBTIMESTAMP"
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
ms.assetid: 1c547d69-a47d-476b-bb74-1f7e1f916b72
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetAsDBTIMESTAMP
Call this member function to convert the time information stored in the `CTime` object to a Win32–compatible <xref:System.Data.OleDb.OleDbType.DBTimeStamp?qualifyHint=False> structure.  
  
## Syntax  
  
```  
bool GetAsDBTIMESTAMP(  
   DBTIMESTAMP& dbts  
) const throw( );  
```  
  
#### Parameters  
 `dbts`  
 A reference to a <xref:System.Data.OleDb.OleDbType.DBTimeStamp?qualifyHint=False> structure containing the current local time.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Stores the resulting time in the referenced `dbts` structure. The **DBTIMESTAMP** data structure initialized by this function will have its **fraction** member set to zero.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#150](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#150)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)