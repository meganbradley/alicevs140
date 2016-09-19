---
title: "Properties and Methods Extended by Project Subtypes"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2b9833bf-8551-4ae1-93db-197ba645c65e
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Properties and Methods Extended by Project Subtypes
A project subtype has a lot of power to influence the behavior of the project because it is constructed as an aggregator of a base project. This section summarizes some of the features that can be enhanced or modified by project subtypes.  
  
## Features Gained by Aggregation  
 The following table summarizes many of the methods that aggregation enables project subtypes to override in base projects.  
  
|Methods Overridden by Aggregation|Project Subtype|  
|---------------------------------------|---------------------|  
|From <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy?qualifyHint=False>:<br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetProperty?qualifyHint=False><br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.SetProperty?qualifyHint=False><br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetGuidProperty?qualifyHint=False><br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.SetGuidProperty?qualifyHint=False>|Enables a project subtype to<br /><br /> -   Change caption and icon of project node.<br />-   Completely override project `Browse` object.<br />-   Control whether project can be renamed.<br />-   Control sort order.<br />-   Control user context for dynamic help.|  
|From <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject?qualifyHint=False>:<br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject.GetItemContext?qualifyHint=False>|Enables a project subtype to control what contextual services are provided to designers and editors.|  
|From <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget?qualifyHint=False>:<br /><br /> <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus?qualifyHint=False><br /><br /> <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.Exec?qualifyHint=False><br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.QueryStatusCommand?qualifyHint=False><br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.ExecCommand?qualifyHint=False>|Enables a project subtype to<br /><br /> -   Participate in the command routing for project commands.<br />-   Add, remove, or disable both project ambient commands and Solution Explorer active commands.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsFilterAddProjectItemDlg2?qualifyHint=False>|Enables the project subtype to filter what the user sees in the **Add New Item** dialog box.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGeneratorFactory?qualifyHint=False>|Enables a project subtype to<br /><br /> -   Determine the default generator given a file extension.<br />-   Map a human readable generator name to a COM object.|  
  
## Properties Used by Project Subtypes  
 The environment and base project system can use the properties from <xref:Microsoft.VisualStudio.Shell.Interop.__VSSPROPID?qualifyHint=False> and <xref:Microsoft.VisualStudio.Shell.Interop.__VSSPROPID2?qualifyHint=False> enumerations detailed in the following table to enable a project subtype to control various features of the project system.  
  
|VSHPROPID property|Project Subtype|  
|------------------------|---------------------|  
|`AddItemTemplatesGuid`|Allows a project subtype to control the contents of the **Add Item** dialog box. The project subtype can provide a new specification of template directories, add new kinds of items, remove existing items, and reorganize a subset of the items in the base project's **Add Item** dialog box.|  
|`PropertyPagesCLSIDList`|Allows a project subtype to add or remove configuration-independent property pages.|  
|`CfgPropertyPagesCLSIDList`|Allows a project subtype to add or remove configuration-dependent property pages.|  
|`ExtObjectCATID`|Allows a project subtype to provide an Automation Extender for the project or project item objects by knowing the Extender CATID. For example, a project subtype can provide a custom `Project.Extender("<subtype>")` object.|  
|`BrowseObjectCATID`|Allows a project subtype to provide an Automation Extender for the `Browse` object by knowing the Extender CATID. For example, a project subtype can add extra properties to the <xref:EnvDTE.Project.Properties?qualifyHint=False> collection.|  
|`CfgBrowseObjectCATID`|Allows a project subtype to provide an Automation Extender for the project configuration browse object. For example, a project subtype can add extra properties to the <xref:EnvDTE.Configuration.Properties?qualifyHint=False> collection.|  
|`CfgExtObjectCATID`|Allows a project subtype to provide an Automation Extender for the configuration object.|  
|`DefaultPlatformName`|Allows a project subtype to determine the platform name for the project's configuration objects.|  
  
 The base project provides a default implementation of the above properties. The base project gets these by calling `QueryInterface` for <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy?qualifyHint=False> on the outermost project subtype, thus allowing the project subtype to override the implementation of the properties.  
  
## See Also  
 [Project Subtypes](../Topic/Project%20Subtypes%20Design.md)