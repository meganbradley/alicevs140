---
title: "COleDateTime::GetAsDBTIMESTAMP"
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
ms.assetid: 8d59a5af-786b-4169-8845-20cebac9fd9e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::GetAsDBTIMESTAMP
Call this method to obtain the time in the `COleDateTime` object as a **DBTIMESTAMP** data structure.  
  
## Syntax  
  
```  
  
      bool GetAsDBTIMESTAMP(  
   DBTIMESTAMP& dbts  
) const throw();  
```  
  
#### Parameters  
 `dbts`  
 A reference to a <xref:System.Data.OleDb.OleDbType.DBTimeStamp?qualifyHint=False> structure.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Stores the resulting time in the referenced `dbts` structure. The **DBTIMESTAMP** data structure initialized by this function will have its **fraction** member set to zero.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#4](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#4)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)