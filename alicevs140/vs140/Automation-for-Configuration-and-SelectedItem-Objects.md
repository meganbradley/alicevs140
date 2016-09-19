---
title: "Automation for Configuration and SelectedItem Objects"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 120377f1-51aa-4445-b2f7-06ab7fc2b47f
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Automation for Configuration and SelectedItem Objects
You can automate the build and selected item processes in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
## Automation for Builds  
 Build or configuration has an automation model that is provided when you implement <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider?qualifyHint=False>. For more information, see [Understanding Build Configurations](../vs140/Understanding-Build-Configurations.md).  
  
 If you create a VSPackage and want to control configuration options, you must use the automation model.  
  
## Automation for SelectedItem  
 You do not have to provide an implementation for the `SelectedItem` object because Visual Studio contains a standard implementation. However, you can implement the `SelectedItem` object if you prefer. You must implement an object that contains the `SelectedItem` interface and return a response to a call to the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage?qualifyHint=False> method with VSITEMID set to <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID.VSHPROPID_ExtSelectedItem?qualifyHint=False>.  
  
## See Also  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage?qualifyHint=False>   
 [Contributing to the Automation Model](../vs140/Contributing-to-the-Automation-Model.md)   
 [Understanding Build Configurations](../vs140/Understanding-Build-Configurations.md)