---
title: "Enumerators"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a60030c5-e1d1-47e1-84bb-cbfe838ab479
caps.latest.revision: 21
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Enumerators
This section lists the enumerator data types in the Source Control Plug-in API that the source control plug-in must know about.  
  
## In This Section  
 [Command Code](../vs140/Command-Code-Enumerator.md)  
 Enumerates the options for the [SccGetCommandOptions Function](../vs140/SccGetCommandOptions-Function.md) and [SccPopulateList Function](../vs140/SccPopulateList-Function.md) functions.  
  
 [Message](../vs140/Message-Enumerator.md)  
 Enumerates flags used for the print callback, [LPTEXTOUTPROC](../vs140/LPTEXTOUTPROC.md).  
  
 [File Status Code](../vs140/File-Status-Code-Enumerator.md)  
 Contains named constant values that specify the state of a file under source control.  
  
 [Directory Status Code](../vs140/Directory-Status-Code-Enumerator.md)  
 Contains named constant values that specify the state of a directory under source control.  
  
## Related Sections  
 [Creating a Source Control Plug-in](../vs140/Creating-a-Source-Control-Plug-in.md)  
 Defines the Source Control Plug-in SDK and describes the included resources.  
  
 [SccGetCommandOptions Function](../vs140/SccGetCommandOptions-Function.md)  
 Prompts the user for advanced options for the given command.  
  
 [SccPopulateList Function](../vs140/SccPopulateList-Function.md)  
 Examines the list of files for their current status. In addition, uses the `pfnPopulate` function to notify the caller when a file does not match the criteria for the `nCommand`.  
  
 [LPTEXTOUTPROC](../vs140/LPTEXTOUTPROC.md)  
 Describes the callback function that is used by [SccOpenProject Function](../vs140/SccOpenProject-Function.md) to display messages from the source control plug-in through the IDE.  
  
 [Source Control Plug-ins](../vs140/Source-Control-Plug-ins.md)  
 Provides a complete listing of all the elements in the Source Control Plug-in API.