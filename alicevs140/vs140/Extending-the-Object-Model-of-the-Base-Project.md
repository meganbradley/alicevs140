---
title: "Extending the Object Model of the Base Project"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2f95cc53-dff6-476c-bacd-500fb0ff7725
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Extending the Object Model of the Base Project
A project subtype may extend the automation object model of the base project in the following places:  
  
-   Project.Extender("<ProjectSubtypeName\>") – This allows a project subtype to offer an object with custom methods from the <xref:EnvDTE.Project?qualifyHint=False>. A project subtype can use Automation Extenders to expose the `Project` object. The <xref:EnvDTE80.IInternalExtenderProvider?qualifyHint=False>interface implemented on the main project subtype aggregator should offer its object for the `VSHPROPID_ExtObjectCATID` from <xref:Microsoft.VisualStudio.Shell.Interop.__VSSPROPID2?qualifyHint=False> (corresponding to an `itemid` value of VSITEMID_ROOT, from `VSITEMID`) CATID.  
  
-   ProjectItem.Extender("<ProjectSubtypeName\>") – This allows a project subtype to offer an object with custom methods from a particular <xref:EnvDTE.ProjectItem?qualifyHint=False> object within the project. A project subtype can use Automation Extenders to expose this object. The <xref:EnvDTE80.IInternalExtenderProvider?qualifyHint=False> interface implemented on the main project subtype aggregator needs to offer its object for the `VSHPROPID_ExtObjectCATID` from <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2?qualifyHint=False> (corresponding to a desired `VSITEMID`) CATID.  
  
-   Project.Properties – This collection exposes the configuration independent properties of the `Project` object. For more information on Project Properties, see <xref:EnvDTE.Project.Properties?qualifyHint=False>. A project subtype can use Automation Extenders to add its properties to this collection. The <xref:EnvDTE80.IInternalExtenderProvider?qualifyHint=False> interface implemented on the main project subtype aggregator needs to offer its object for the `VSHPROPID_BrowseObjectCATID` from VSHPROPID2 (corresponding to an `itemid` value of VSITEMID_ROOT, from <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2?qualifyHint=False>) CATID.  
  
-   Configuration.Properties – This collection exposes the configuration dependent properties of the project for a particular configuration (for example, Debug). For more information see, <xref:EnvDTE.Configuration?qualifyHint=False>. A project subtype can use Automation Extenders to add its properties to this collection. The <xref:EnvDTE80.IInternalExtenderProvider?qualifyHint=False> interface implemented on the main project subtype aggregator offers its object for the CATID `VSHPROPID_CfgBrowseObjectCATID` (corresponding to an `itemid` value of <xref:Microsoft.VisualStudio.VSConstants.VSITEMID_ROOT?qualifyHint=False>). The <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgBrowseObject?qualifyHint=False>interface is used to distinguish one configuration browse object from another.  
  
## See Also  
 <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID?qualifyHint=False>