---
title: "pgomgr"
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
ms.assetid: 74589126-df18-42c9-8739-26d60e148d6a
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# pgomgr
Adds profile data from one or more .pgc files to the .pgd file.  
  
## Syntax  
  
```  
pgomgr [options] pgcfiles pgdfile  
```  
  
#### Parameters  
 `options`  
 The following options can be specified to pgomgr:  
  
 **/help—**Displays available pgomgr options (short for /?).  
  
 **/clear—**Causes the .pgd file to be cleared of all profile information. You cannot specify a .pgc file when **/clear** is specified.  
  
 **/detail**—Displays detailed statistics, including flow graph coverage information.  
  
 **/summary**—Displays per-function statistics.  
  
 **/unique**—when used with **/summary**, causes decorated function names to display.  The default, when /unique is not used, is for undecorated function names to be displayed.  
  
 **/merge**[**:***n*]**—**Causes the data in the .pgc file or files to be added to the .pgd file.  The optional parameter, *n*, lets you specify hat the data should be added *n* times.  For example, if a scenario would commonly be done 6 times, you can do it once in a test run and add it to the .pgd file six times with **pgomgr /merge:6**.  
  
 `pgcfiles`  
 One or more .pgc files whose profile data you want to merge into the .pgd file. You can specify a single .pgc file or multiple .pgc files. If you do not specify any .pgc files, pgomgr will merge all .pgc files whose filenames are the same as the .pgd file.  
  
 `pgdfile`  
 The .pgd file into which you are merging data from the .pgc file or files.  
  
## Remarks  
  
> [!NOTE]
>  You can start this tool only from the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] command prompt. You cannot start it from a system command prompt or from File Explorer.  
  
## Example  
 In the following example, the .pgd file was cleared of profile data.  
  
```  
pgomgr /clear myapp.pgd  
```  
  
 In the following example, the profile data in myapp1.pgc was added to the .pgd file 3 times.  
  
```  
pgomgr /merge:3 myapp1.pgc myapp.pgd  
```  
  
 In the following example, profile data from all myapp#.pgc files is added to the myapp.pgd file.  
  
```  
pgomgr -merge myapp1.pgd  
```  
  
## See Also  
 [Tools for Manual Profile-Guided Optimization](../vs140/Tools-for-Manual-Profile-Guided-Optimization.md)