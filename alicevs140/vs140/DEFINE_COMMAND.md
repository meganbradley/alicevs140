---
title: "DEFINE_COMMAND"
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
ms.assetid: 9d724968-e242-413c-9a13-e7175fccf9b1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DEFINE_COMMAND
Specifies the command that will be used to create the rowset when using the [CCommand](../vs140/CCommand-Class.md) class. Accepts only string types matching the specified application type (ANSI or Unicode).  
  
> [!NOTE]
>  It is recommended that you use [DEFINE_COMMAND_EX](../vs140/DEFINE_COMMAND_EX.md) instead of `DEFINE_COMMAND`.  
  
## Syntax  
  
```  
  
DEFINE_COMMAND(  
x  
,   
szCommand  
 )  
  
```  
  
#### Parameters  
 *x*  
 [in] The name of the user record (command) class.  
  
 `szCommand`  
 [in] The command string that will be used to create the rowset when using [CCommand](../vs140/CCommand-Class.md).  
  
## Remarks  
 The command string that you specify will be used as the default if you do not specify command text in the [CCommand::Open](../vs140/CCommand--Open.md) method.  
  
 This macro accepts ANSI strings if you build your application as ANSI, or Unicode strings if you build your application as Unicode. It is recommended that you use [DEFINE_COMMAND_EX](../vs140/DEFINE_COMMAND_EX.md) instead of `DEFINE_COMMAND`, because the former accepts Unicode strings, regardless of the ANSI or Unicode application type.  
  
## Example  
 See [BOOKMARK_ENTRY](../vs140/BOOKMARK_ENTRY.md).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md)