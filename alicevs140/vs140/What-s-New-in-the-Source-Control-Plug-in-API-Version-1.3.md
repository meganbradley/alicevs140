---
title: "What&#39;s New in the Source Control Plug-in API Version 1.3"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7dfb2227-6e1d-4028-bce9-f8967456a993
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# What&#39;s New in the Source Control Plug-in API Version 1.3
The Source Control Plug-in API version 1.3 introduces the following new functions to provide more advanced control.  
  
## Changes  
 The following functions are new to the Source Control Plug-in API version 1.3:  
  
|Function|Overview|  
|--------------|--------------|  
|[SccGetExtendedCapabilities](../vs140/SccGetExtendedCapabilities-Function.md)|Allows additional capability bits to be reported|  
|[SccEnumChangedFiles](../vs140/SccEnumChangedFiles-Function.md)|Allows examination of files that have newer versions in the version control database than on the local disk|  
|[SccQueryChanges](../vs140/SccQueryChanges-Function.md)|Allows examination of the state of name changes (renames, additions, and deletions) for specified files|  
|[SccPopulateDirList](../vs140/SccPopulateDirList-Function.md)|Allows examination of directories and files in the version control database|  
|[SccAddFilesFromSCC](../vs140/SccAddFilesFromSCC-Function.md)|Adds a specified list of files from the version control database to the current project|  
|[SccBackgroundGet](../vs140/SccBackgroundGet-Function.md)|Performs a silent "Get" of the specified files (no user interface is shown)|  
|[SccGetUserOption](../vs140/SccGetUserOption-Function.md)|Allows access to user-specific options|  
  
## See Also  
 [Getting Started (Source Control Plug-ins)](../vs140/Getting-Started-with-Source-Control-Plug-ins.md)   
 [What's New in the Source Control Plug-in API Version 1.2](../vs140/What-s-New-in-the-Source-Control-Plug-in-API-Version-1.2.md)