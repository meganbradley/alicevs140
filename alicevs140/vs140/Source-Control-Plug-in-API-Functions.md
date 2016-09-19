---
title: "Source Control Plug-in API Functions"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4b0536dd-4f92-4ef2-9031-4548281f37aa
caps.latest.revision: 21
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Source Control Plug-in API Functions
The Source Control Plug-in API provides the following functions, which must be implemented by the source control plug-in in accordance with this API. The signatures of each function and the semantics associated with the bit flags and other parameters are described in detail in this reference.  
  
## Initialization and Housekeeping Functions  
  
|Function|Description|  
|--------------|-----------------|  
|[SccCloseProject](../vs140/SccCloseProject-Function.md)|Closes a project.|  
|[SccGetCommandOptions](../vs140/SccGetCommandOptions-Function.md)|Prompts the user for advanced options for the given command.|  
|[SccGetVersion](../vs140/SccGetVersion-Function.md)|Returns the version of the source control plug-in.|  
|[SccInitialize](../vs140/SccInitialize-Function.md)|Initializes the source control plug-in. It is called once for each instance of the plug-in.|  
|[SccOpenProject](../vs140/SccOpenProject-Function.md)|Opens a project.|  
|[SccSetOption](../vs140/SccSetOption-Function.md)|A generic function used to set a wide variety of options. Each option starts with `SCC_OPT_xxx` and has its own defined set of values.|  
|[SccUninitialize](../vs140/SccUninitialize-Function.md)|Called once when a source control plug-in needs to be unplugged.|  
  
## Core Source Control Functions  
  
|Function|Description|  
|--------------|-----------------|  
|[SccAdd](../vs140/SccAdd-Function.md)|Adds an array of files specified by fully qualified path names to the source control system.|  
|[SccAddFromScc](../vs140/SccAddFromScc-Function.md)|Allows the user to browse for files that are already in the source control system and then make those files part of the current project.|  
|[SccCheckin](../vs140/SccCheckin-Function.md)|Checks in an array of files.|  
|[SccCheckout](../vs140/SccCheckout-Function.md)|Checks out an array of files.|  
|[SccDiff](../vs140/SccDiff-Function.md)|Shows the differences between the local user's file specified by a fully qualified path name and the version under source control.|  
|[SccGet](../vs140/SccGet-Function.md)|Retrieves a read-only copy of a set of files.|  
|[SccGetEvents](../vs140/SccGetEvents-Function.md)|Checks the status of files that the caller has asked about (via `SccQueryInfo`).|  
|[SccGetProjPath](../vs140/SccGetProjPath-Function.md)|Causes the source control plug-in to prompt the user for a project path that is meaningful to the plug-in.|  
|[SccHistory](../vs140/SccHistory-Function.md)|Shows the history for an array of fully qualified local file names.|  
|[SccPopulateList](../vs140/SccPopulateList-Function.md)|Examines the list of files for their current status. In addition, uses the `pfnPopulate` function to notify the caller when a file does not match the criteria for the `nCommand`.|  
|[SccProperties](../vs140/SccProperties-Function.md)|Shows the properties of a fully qualified file.|  
|[SccQueryInfo](../vs140/SccQueryInfo-Function.md)|Examines a list of fully qualified files for their current status.|  
|[SccRemove](../vs140/SccRemove-Function.md)|Removes the array of fully qualified files from the source control system.|  
|[SccRename](../vs140/SccRename-Function.md)|Renames the given file to a new name in the source control system.|  
|[SccRunScc](../vs140/SccRunScc-Function.md)|Accesses the full range of features of the source control system.|  
|[SccUncheckout](../vs140/SccUncheckout-Function.md)|Undoes a checkout of an array of files.|  
  
## Functions that Support Additional Capability (Version 1.2 of the Source Control Plug-in API)  
 This group of functions defines the additional functionality included in version 1.2 of the Source Control Plug-in API. They provide access to more advanced source control features and capabilities.  
  
|Function|Description|  
|--------------|-----------------|  
|[SccBeginBatch](../vs140/SccBeginBatch-Function.md)|Starts a batch operation.|  
|[SccCreateSubProject](../vs140/SccCreateSubProject-Function.md)|Creates a subproject with the given name under an existing parent project.|  
|[SccDirDiff](../vs140/SccDirDiff-Function.md)|Shows the differences between the local user's directory specified by a fully qualified path name and the source control database location.|  
|[SccDirQueryInfo](../vs140/SccDirQueryInfo-Function.md)|Examines a list of fully qualified directories for their current status.|  
|[SccEndBatch](../vs140/SccEndBatch-Function.md)|Ends a batch operation.|  
|[SccGetParentProjectPath](../vs140/SccGetParentProjectPath-Function.md)|Returns parent path of the given project (the project must exist).|  
|[SccIsMultiCheckoutEnabled](../vs140/SccIsMultiCheckoutEnabled-Function.md)|Checks whether multiple checkouts on a file are allowed.|  
|[SccWillCreateSccFile](../vs140/SccWillCreateSccFile-Function.md)|Checks whether the plug-in will create MSSCCPRJ.SCC files.|  
  
## Functions that Support Advanced Capability (Version 1.3 of the Source Control Plug-in API)  
 This group of functions defines the additional functionality included in version 1.3 of the Source Control Plug-in API. They provide access to more advanced source control features and capabilities.  
  
|Function|Description|  
|--------------|-----------------|  
|[SccAddFilesFromSCC](../vs140/SccAddFilesFromSCC-Function.md)|Adds a list of files from source control to the current project.|  
|[SccBackgroundGet](../vs140/SccBackgroundGet-Function.md)|Retrieves a list of files from source control without a user interface.|  
|[SccEnumChangedFiles](../vs140/SccEnumChangedFiles-Function.md)|Retrieves a list of files in source control that are different from the local files.|  
|[SccGetExtendedCapabilities](../vs140/SccGetExtendedCapabilities-Function.md)|Retrieves flags that specify extended capabilities supported by the source control plug-in.|  
|[SccGetUserOption](../vs140/SccGetUserOption-Function.md)|Retrieves user-specific options.|  
|[SccPopulateDirList](../vs140/SccPopulateDirList-Function.md)|Examines a list of directories and files in a project or projects that are under source control. Each directory and file name found is passed to a callback function.|  
|[SccQueryChanges](../vs140/SccQueryChanges-Function.md)|Examines name changes made to a list of files. Each file name is passed to a callback function with its change status.|  
  
## Requirements  
 Header: scc.h  
  
 (Supplied in the Environment SDK common includes folder, by default *[drive]*\Program Files\VSIP 8.0\EnvSDK\common\inc; also supplied in the VSIP folder with the MSSCCI sample, *[drive]*\Program Files\VSIP 8.0\MSSCCI).  
  
## See Also  
 [Source Control Plug-ins](../vs140/Source-Control-Plug-ins.md)   
 [Creating a Source Control Plug-in](../vs140/Creating-a-Source-Control-Plug-in.md)