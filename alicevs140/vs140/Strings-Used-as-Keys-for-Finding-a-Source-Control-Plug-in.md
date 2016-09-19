---
title: "Strings Used as Keys for Finding a Source Control Plug-in"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c1e31f76-42a1-4c3d-afb2-664044ef12fd
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Strings Used as Keys for Finding a Source Control Plug-in
The following strings are the keys for accessing the registry to find information about the source control plug-in.  
  
 `STR_SCC_PROVIDER_REG_LOCATION`, `STR_PROVIDERREGKEY`, `STR_SCCPROVIDERPATH`, and `STR_SCCPROVIDERNAME` are registry keys or values used to register a DLL as a source control plug-in for Visual Studio.  
  
 `SCC_PROJECTNAME_KEY`, `SCC_PROJECTAUX_KEY`, `SCC_KEY, SCC_FILE_SIGNATURE`, and `SCC_STATUS_FILE` are used to describe the format of the MSSCCPRJ.SCC file.  
  
## String Keys and Values  
  
|Key|Value|  
|---------|-----------|  
|`STR_SCC_PROVIDER_REG_LOCATION`|Software\SourceCodeControlProvider|  
|`STR_PROVIDERREGKEY`|ProviderRegKey|  
|`STR_SCCPROVIDERPATH`|SCCServerPath|  
|`STR_SCCPROVIDERNAME`|SCCServerName|  
|`STR_SCC_INI_SECTION`|Source Code Control|  
|`STR_SCC_INI_KEY`|SourceCodeControlProvider|  
|`SCC_PROJECTNAME_KEY`|SCC_Project_Name|  
|`SCC_PROJECTAUX_KEY`|SCC_Aux_Path|  
|`SCC_STATUS_FILE`|MSSCCPRJ.SCC|  
|`SCC_KEY`|SCC|  
|`SCC_FILE_SIGNATURE`|A source code control file|  
|`SCC_NSE`|Namespace extension|  
|`SCC_NSE_PREFIX`|Protocal Prefix|  
|`SCC_NSE_DisableOpenSCC`|DisableOpenFromSourceControl|  
|`STR_SCCHELPCOLLECTION`|HelpCollection|  
|`STR_UI_LANGUAGE`|UILanguage|  
|`STR_SRCSAFE_ROOT_KEY`|Software\Microsoft\SourceSafe|  
  
## See Also  
 [Source Control Plug-ins](../vs140/Source-Control-Plug-ins.md)   
 [How to: Install a Source Control Plug-in](../vs140/How-to--Install-a-Source-Control-Plug-in.md)   
 [MSSCCPRJ.SCC File](../vs140/MSSCCPRJ.SCC-File.md)