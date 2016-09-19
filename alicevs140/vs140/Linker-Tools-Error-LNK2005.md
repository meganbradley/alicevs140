---
title: "Linker Tools Error LNK2005"
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
ms.topic: error-reference
ms.assetid: d9587adc-68be-425c-8a30-15dbc86717a4
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK2005
symbol already defined in object  
  
 The given `symbol`, displayed in its decorated form, was multiply defined.  
  
 For more information, see the Knowledge Base articles:  
  
-   "LNK2005 Errors When Link C Run-Time Libraries Are Linked Before MFC Libraries" (Q148652)  
  
-   "Global Overloaded Delete Operator Causes LNK2005" (Q140440)  
  
-   "LNK2005 Errors on New and Delete When Defining _ATL_MIN_CRT" (Q184235).  
  
 You can find Knowledge Base articles on the MSDN Library CD-ROM or at [http://support.microsoft.com/search](http://support.microsoft.com/search).  
  
 This error is followed by fatal error [LNK1169](../vs140/Linker-Tools-Error-LNK1169.md).  
  
### To fix by checking the following possible causes  
  
1.  Mixing static and dynamic libraries when also using [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
2.  The symbol is a packaged function (created by compiling with [/Gy](../vs140/-Gy--Enable-Function-Level-Linking-.md)) and was included in more than one file but was changed between compilations. Recompile all files that include `symbol`.  
  
3.  The symbol is defined differently in two member objects in different libraries, and both member objects were used.  
  
4.  An absolute is defined twice, with a different value in each definition.  
  
5.  A header file declared and defined a variable. Possible solutions include:  
  
    -   Declare the variable in .h: `extern BOOL MyBool;` and then assign to it in a .c or .cpp file: `BOOL MyBool = FALSE;`.  
  
    -   Declare the variable [static](../vs140/Static--C---.md).  
  
    -   Declare the variable [selectany](../vs140/selectany.md).  
  
6.  If you use uuid.lib in combination with other .lib files that define GUIDs (for example, oledb.lib and adsiid.lib). For example:  
  
    ```  
    oledb.lib(oledb_i.obj) : error LNK2005: _IID_ITransactionObject  
    already defined in uuid.lib(go7.obj)  
    ```  
  
     To fix, add [/FORCE:MULTIPLE](../vs140/-FORCE--Force-File-Output-.md) to the linker command line options, and make sure that uuid.lib is the first library referenced.