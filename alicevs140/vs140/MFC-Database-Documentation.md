---
title: "MFC Database Documentation"
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
ms.assetid: bb120282-cd0d-4bf4-a27c-93b3501fb3a0
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC Database Documentation
The MFC documentation for DAO and ODBC classes consists of the components listed in the following table.  
  
### MFC Database Documentation  
  
|For documentation about|See|  
|-----------------------------|---------|  
|Classes for both DAO and ODBC|The class name in the *MFC Reference*|  
|Global functions and macros for both DAO and ODBC|The function or macro name in the *MFC Reference*|  
|Programming with the MFC ODBC classes|[ODBC and MFC](../vs140/ODBC-and-MFC.md)|  
|Technical notes for both DAO and ODBC|[MFC Technical Notes](../vs140/Technical-Notes-by-Category.md)|  
  
##  <a name="_core_mfc_documentation_and_dao_documentation"></a> MFC Documentation and DAO Documentation  
 Throughout the MFC documentation for the MFC DAO classes, you will find references to topics in the DAO SDK documentation, included in the online documentation. Because MFC encapsulates (or wraps) DAO, the MFC documentation:  
  
-   Focuses on MFC and how it differs from the underlying DAO implementation.  
  
-   Points you to the DAO SDK Help topics for the underlying details. These cross-references are always worded as "topic *X* in DAO Help."  
  
-   Points out differences where MFC does things differently from the way DAO does them. MFC does not wrap all of DAO. For example, MFC does not supply objects for DAO security functionality.  
  
> [!NOTE]
>  The DAO SDK Help is a separate Help file. There are no hypertext links from this documentation to DAO help in this version of Visual C++.  
  
> [!NOTE]
>  You might have to do some translating when you are browsing topics in DAO SDK Help. Examples in the primary DAO SDK documentation are written in the Basic programming language, not C++. (But the DAO SDK supplies a set of C++ examples that do not use MFC.)  
  
##  <a name="_core_mfc_documentation_and_odbc_documentation"></a> MFC Documentation and ODBC Documentation  
 The MFC documentation for the MFC ODBC classes is organized differently. The MFC ODBC classes supply a high-level abstraction that rests on ODBC rather than a wrapper of the ODBC API. Therefore, the two documentation sets are less connected than are the MFC and DAO documentation sets. The ODBC documentation uses the C language, which is much closer to C++ than is Basic.  
  
## See Also  
 [MFC Database Classes (ODBC and DAO)](../vs140/MFC-Database-Classes--ODBC-and-DAO-.md)   
 [ODBC Basics](../vs140/ODBC-Basics.md)