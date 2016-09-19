---
title: "Deploying Project Types"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7f132f67-8589-464c-90dc-0d57ae02aa8f
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Deploying Project Types
[!INCLUDE[vsipsdk](../vs140/includes/vsipsdk_md.md)] installs a new project-type aggregator (ProjectAggregator2.dll) and also a Windows Installer package for redistribution (ProjectAggregator2.msi). You must use the new aggregator for managed-code project types. ProjectAggregator2 works arounds limitations in the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] project aggregator that prevent managed-code project types from working correctly. The following steps describe how to change your VSPackage to use the new aggregator.  
  
1.  Remove the NativeHierarchyWrapper project from your solution.  
  
2.  Remove any NativeHierarchyWrapper binaries from your setup.  
  
3.  Add ProjectAggregator2.msi to your setup.