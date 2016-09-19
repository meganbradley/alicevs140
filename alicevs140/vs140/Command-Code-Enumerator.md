---
title: "Command Code Enumerator"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5d2c360c-59e4-4da8-bcb4-dd07c7441e40
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Command Code Enumerator
This enumerator is used in the options for the [SccGetCommandOptions Function](../vs140/SccGetCommandOptions-Function.md) and the [SccPopulateList Function](../vs140/SccPopulateList-Function.md)to indicate the command for which the options are specified.  
  
## Syntax  
  
```  
enum SCCCOMMAND {  
   SCC_COMMAND_GET,  
   SCC_COMMAND_CHECKOUT,  
   SCC_COMMAND_CHECKIN,  
   SCC_COMMAND_UNCHECKOUT,  
   SCC_COMMAND_ADD,  
   SCC_COMMAND_REMOVE,  
   SCC_COMMAND_DIFF,  
   SCC_COMMAND_HISTORY,  
   SCC_COMMAND_RENAME,  
   SCC_COMMAND_PROPERTIES,  
   SCC_COMMAND_OPTIONS  
};  
```  
  
## Members  
 SCC_COMMAND_GET  
 Corresponds to the [SccGet Function](../vs140/SccGet-Function.md).  
  
 SCC_COMMAND_CHECKOUT  
 Corresponds to the [SccCheckout Function](../vs140/SccCheckout-Function.md).  
  
 SCC_COMMAND_CHECKIN  
 Corresponds to the [SccCheckin Function](../vs140/SccCheckin-Function.md).  
  
 SCC_COMMAND_UNCHECKOUT  
 Corresponds to the [SccUncheckout Function](../vs140/SccUncheckout-Function.md).  
  
 SCC_COMMAND_ADD  
 Corresponds to the [SccAdd Function](../vs140/SccAdd-Function.md).  
  
 SCC_COMMAND_REMOVE  
 Corresponds to the [SccRemove Function](../vs140/SccRemove-Function.md).  
  
 SCC_COMMAND_DIFF  
 Corresponds to the [SccDiff Function](../vs140/SccDiff-Function.md).  
  
 SCC_COMMAND_HISTORY  
 Corresponds to the [SccHistory Function](../vs140/SccHistory-Function.md).  
  
 SCC_COMMAND_RENAME  
 Corresponds to the [SccRename Function](../vs140/SccRename-Function.md).  
  
 SCC_COMMAND_PROPERTIES  
 Corresponds to the [SccProperties Function](../vs140/SccProperties-Function.md).  
  
 SCC_COMMAND_OPTIONS  
 Corresponds to the [SccSetOption Function](../vs140/SccSetOption-Function.md).  
  
## See Also  
 [Source Control Plug-ins](../vs140/Source-Control-Plug-ins.md)   
 [SccGetCommandOptions Function](../vs140/SccGetCommandOptions-Function.md)   
 [SccPopulateList Function](../vs140/SccPopulateList-Function.md)