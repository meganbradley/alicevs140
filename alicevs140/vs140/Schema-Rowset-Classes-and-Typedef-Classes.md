---
title: "Schema Rowset Classes and Typedef Classes"
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
ms.assetid: 4bd881b3-26ca-4bdb-9226-d67560864f29
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Schema Rowset Classes and Typedef Classes
A schema is a collection of database objects that are owned, or have been created by, a particular user. A catalog can contain one or more schemas, but must always contain a schema called INFORMATION_SCHEMA, which contains the views and domains of the information schema. Schema information in OLE DB is retrieved using predefined schema rowsets, and includes types, tables, columns, indexes, views, assertions and constraints, statistics, character sets, collations, and domains.  
  
 Schema rowsets are predefined rowsets representing metadata. Schema rowsets are generally used in dynamic programming, where the database structure is not known at compile time. You can use these schema rowsets to obtain information about a database at run time.  
  
 Use the typedef classes to instantiate the schema rowsets. The corresponding typedef and schema rowset classes are listed below. You must call [CRestrictions::Open](../vs140/CRestrictions--Open.md) after you have created an instance of the schema rowset. This method returns a result set based on the restrictions you specify. See [IDBSchemaRowset](https://msdn.microsoft.com/en-us/library/ms713686.aspx) for information on restriction columns associated with each schema rowset.  
  
 The following table displays each OLE DB Schema Rowset and its corresponding OLE DB Templates typedef class and info class.  
  
|OLE DB Schema Rowset|Typedef class|Info class|  
|--------------------------|-------------------|----------------|  
|[ASSERTIONS](https://msdn.microsoft.com/en-us/library/ms719776.aspx)|[CAssertions](../vs140/CAssertions--CAssertionInfo.md)|[CAssertionInfo](../vs140/CAssertions--CAssertionInfo.md)|  
|[CATALOGS](https://msdn.microsoft.com/en-us/library/ms721241.aspx)|[CCatalogs](../vs140/CCatalogs--CCatalogInfo.md)|[CCatalogInfo](../vs140/CCatalogs--CCatalogInfo.md)|  
|[CHARACTER_SETS](https://msdn.microsoft.com/en-us/library/ms722638.aspx)|[CCharacterSets](../vs140/CCharacterSets--CCharacterSetInfo.md)|[CCharacterSetInfo](../vs140/CCharacterSets--CCharacterSetInfo.md)|  
|[COLLATIONS](https://msdn.microsoft.com/en-us/library/ms715783.aspx)|[CCollations](../vs140/CCollations--CCollationInfo.md)|[CCollationInfo](../vs140/CCollations--CCollationInfo.md)|  
|[COLUMN_PRIVILEGES](https://msdn.microsoft.com/en-us/library/ms715800.aspx)|[CColumnPrivileges](../vs140/CColumnPrivileges--CColumnPrivilegeInfo.md)|[CColumnPrivilegeInfo](../vs140/CColumnPrivileges--CColumnPrivilegeInfo.md)|  
|[COLUMNS](https://msdn.microsoft.com/en-us/library/ms723052.aspx)|[CColumns](../vs140/CColumns--CColumnsInfo.md)|[CColumnsInfo](../vs140/CColumns--CColumnsInfo.md)|  
|[CONSTRAINT_COLUMN_USAGE](https://msdn.microsoft.com/en-us/library/ms724522.aspx)|[CConstraintColumnUsage](../vs140/CConstraintColumnUsage--CConstraintColumnUsageInfo.md)|[CConstraintColumnUsageInfo](../vs140/CConstraintColumnUsage--CConstraintColumnUsageInfo.md)|  
|[CONSTRAINT_TABLE_USAGE](https://msdn.microsoft.com/en-us/library/ms713710.aspx)|[CConstraintTableUsage](../vs140/CConstraintTableUsage--CConstraintTableUsageInfo.md)|[CConstraintTableUsageInfo](../vs140/CConstraintTableUsage--CConstraintTableUsageInfo.md)|  
|[CHECK_CONSTRAINTS](https://msdn.microsoft.com/en-us/library/ms712845.aspx)|[CCheckConstraints](../vs140/CCheckConstraints--CCheckConstraintInfo.md)|[CCheckConstraintInfo](../vs140/CCheckConstraints--CCheckConstraintInfo.md)|  
|[COLUMN_DOMAIN_USAGE](https://msdn.microsoft.com/en-us/library/ms711240.aspx)|[CColumnDomainUsage](../vs140/CColumnDomainUsage--CColumnDomainUsageInfo.md)|[CColumnDomainUsageInfo](../vs140/CColumnDomainUsage--CColumnDomainUsageInfo.md)|  
|[FOREIGN_KEYS](https://msdn.microsoft.com/en-us/library/ms711276.aspx)|[CForeignKeys](../vs140/CForeignKeys--CForeignKeysInfo.md)|[CForeignKeysInfo](../vs140/CForeignKeys--CForeignKeysInfo.md)|  
|[INDEXES](https://msdn.microsoft.com/en-us/library/ms709712.aspx)|[CIndexes](../vs140/CIndexes--CIndexInfo.md)|[CIndexInfo](../vs140/CIndexes--CIndexInfo.md)|  
|[KEY_COLUMN_USAGE](https://msdn.microsoft.com/en-us/library/ms712990.aspx)|[CKeyColumnUsage](../vs140/CKeyColumns--CKeyColumnInfo.md)|[CKeyColumnUsageInfo](../vs140/CKeyColumns--CKeyColumnInfo.md)|  
|[PRIMARY_KEYS](https://msdn.microsoft.com/en-us/library/ms714362.aspx)|[CPrimaryKeys](../vs140/CPrimaryKeys--CPrimaryKeyInfo.md)|[CPrimaryKeyInfo](../vs140/CPrimaryKeys--CPrimaryKeyInfo.md)|  
|[PROCEDURES](https://msdn.microsoft.com/en-us/library/ms724021.aspx)|[CProcedures](../vs140/CProcedures--CProcedureInfo.md)|[CProcedureInfo](../vs140/CProcedures--CProcedureInfo.md)|  
|[PROCEDURE_COLUMNS](https://msdn.microsoft.com/en-us/library/ms723092.aspx)|[CProcedureColumns](../vs140/CProcedureColumns--CProcedureColumnInfo.md)|[CProcedureColumnInfo](../vs140/CProcedureColumns--CProcedureColumnInfo.md)|  
|[PROCEDURE_PARAMETERS](https://msdn.microsoft.com/en-us/library/ms713623.aspx)|[CProcedureParameters](../vs140/CProcedureParameters-CProcedureParamInfo.md)|[CProcedureParameterInfo](../vs140/CProcedureParameters-CProcedureParamInfo.md)|  
|[PROVIDER_TYPES](https://msdn.microsoft.com/en-us/library/ms709785.aspx)|[CProviderTypes](../vs140/CProviderTypes--CProviderInfo.md)|[CProviderInfo](../vs140/CProviderTypes--CProviderInfo.md)|  
|[REFERENTIAL_CONSTRAINTS](https://msdn.microsoft.com/en-us/library/ms719737.aspx)|[CReferentialConstraints](../vs140/CReferentialConstraints--CReferentialConstraintInfo.md)|[CReferentialConstraintInfo](../vs140/CReferentialConstraints--CReferentialConstraintInfo.md)|  
|[SCHEMATA](https://msdn.microsoft.com/en-us/library/ms716887.aspx)|[CSchemata](../vs140/CSchemata--CSchemataInfo.md)|[CSchemataInfo](../vs140/CSchemata--CSchemataInfo.md)|  
|[SQL_LANGUAGES](https://msdn.microsoft.com/en-us/library/ms714374.aspx)|[CSQLLanguages](../vs140/CSQLLanguages--CSQLLanguageInfo.md)|[CSQLLanguageInfo](../vs140/CSQLLanguages--CSQLLanguageInfo.md)|  
|[STATISTICS](https://msdn.microsoft.com/en-us/library/ms715957.aspx)|[CStatistics](../vs140/CStatistics--CStatisticInfo.md)|[CStatisticInfo](../vs140/CStatistics--CStatisticInfo.md)|  
|[TABLE_CONSTRAINTS](https://msdn.microsoft.com/en-us/library/ms715921.aspx)|[CTableConstraints](../vs140/CTableConstraints--CTableConstraintInfo.md)|[CTableConstraintInfo](../vs140/CTableConstraints--CTableConstraintInfo.md)|  
|[TABLES](https://msdn.microsoft.com/en-us/library/ms716980.aspx)|[CTables](../vs140/CTables--CTableInfo.md)|[CTableInfo](../vs140/CTables--CTableInfo.md)|  
|[TABLE_PRIVILEGES](https://msdn.microsoft.com/en-us/library/ms725428.aspx)|[CTablePrivileges](../vs140/CTablePrivileges--CTablePrivilegeInfo.md)|[CTablePrivilegeInfo](../vs140/CTablePrivileges--CTablePrivilegeInfo.md)|  
|[TRANSLATIONS](https://msdn.microsoft.com/en-us/library/ms725365.aspx)|[CTranslations](../vs140/CTranslations--CTranslationInfo.md)|[CTranslationInfo](../vs140/CTranslations--CTranslationInfo.md)|  
|[USAGE_PRIVILEGES](https://msdn.microsoft.com/en-us/library/ms722743.aspx)|[CUsagePrivileges](../vs140/CUsagePrivileges--CUsagePrivilegeInfo.md)|[CUsagePrivilegeInfo](../vs140/CUsagePrivileges--CUsagePrivilegeInfo.md)|  
|[VIEW_COLUMN_USAGE](https://msdn.microsoft.com/en-us/library/ms714896.aspx)|[CViewColumnUsage](../vs140/CViewColumnUsage--CViewColumnInfo.md)|[CViewColumnInfo](../vs140/CViewColumnUsage--CViewColumnInfo.md)|  
|[VIEWS](https://msdn.microsoft.com/en-us/library/ms723122.aspx)|[CViews](../vs140/CViews--CViewInfo.md)|[CViewInfo](../vs140/CViews--CViewInfo.md)|  
|[VIEW_TABLE_USAGE](https://msdn.microsoft.com/en-us/library/ms719727.aspx)|[CViewTableUsage](../vs140/CViewTableUsage--CViewTableInfo.md)|[CViewTableInfo](../vs140/CViewTableUsage--CViewTableInfo.md)|  
  
## Requirements  
 **Header:** atldbsch.h  
  
## See Also  
 [CRestrictions Class](../vs140/CRestrictions-Class.md)