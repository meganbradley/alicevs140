---
title: "CDataRecoveryHandler::GenerateAutosaveFileName"
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
ms.assetid: 5ebd5359-a4bf-4329-a67e-4ba7cda89e1e
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::GenerateAutosaveFileName
Generates the name for an autosave file associated with the supplied document file name.  
  
## Syntax  
  
```  
virtual CString GenerateAutosaveFileName(  
   const CString &strDocumentName  
) const;  
```  
  
#### Parameters  
 [in] `strDocumentName`  
 A string that contains the document name. `GenerateAutosaveFileName` uses this document name to generate a corresponding autosave file name.  
  
## Return Value  
 The autosave file name generated from `strDocumentName`.  
  
## Remarks  
 Each document name has a one-to-one mapping with an autosave file name.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)