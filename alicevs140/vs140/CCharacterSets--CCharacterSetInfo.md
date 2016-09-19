---
title: "CCharacterSets, CCharacterSetInfo"
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
ms.topic: article
ms.assetid: 029d068c-8bb2-4fc0-8709-78ce7f74446e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCharacterSets, CCharacterSetInfo
Call the typedef class **CCharacterSets** to implement its parameter class **CCharacterSetInfo**.  
  
## Remarks  
 See [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md) for more information on using typedef classes.  
  
 This class identifies the character sets defined in the catalog that are accessible to a given user.  
  
 The following table lists the class data members and their corresponding OLE DB Columns. See [CHARACTER_SETS Rowset](https://msdn.microsoft.com/en-us/library/ms722638.aspx) in the *OLE DB Programmer's Reference* for more information about the schema and columns.  
  
|Data members|OLE DB columns|  
|------------------|--------------------|  
|m_szCatalog|CHARACTER_SET_CATALOG|  
|m_szSchema|CHARACTER_SET_SCHEMA|  
|m_szName|CHARACTER_SET_NAME|  
|m_szFormOfUse|FORM_OF_USE|  
|m_nNumCharacters|NUMBER_OF_CHARACTERS|  
|m_szCollateCatalog|DEFAULT_COLLATE_CATALOG|  
|m_szCollateSchema|DEFAULT_COLLATE_SCHEMA|  
|m_szCollateName|DEFAULT_COLLATE_NAME|  
  
## Requirements  
 **Header:** atldbsch.h  
  
## See Also  
 [CRestrictions Class](../vs140/CRestrictions-Class.md)