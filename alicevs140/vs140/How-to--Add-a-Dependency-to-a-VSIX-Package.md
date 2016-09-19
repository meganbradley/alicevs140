---
title: "How to: Add a Dependency to a VSIX Package"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8f20177b-dab9-43a3-b959-81a591b451d6
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# How to: Add a Dependency to a VSIX Package
You can set up a VSIX package deployment that installs any dependencies that are not already present on the target computer. To accomplish this, include the VSIX dependencies to the source.extension.vsixmanifest file.  
  
#### To add a dependency  
  
1.  Open the source.extension.vsixmanifest file in the **Design** view. Go to the **Dependencies** tab and click **New**.  
  
2.  To add an installed extension: in the **Add New Dependency** dialog box, select **Installed extension** and then, for the **Name**, select an extension on the list.  
  
3.  To add another VSIX that is not installed: : in the **Add New Dependency** dialog box, select **File on file system** and then use the **Browse** button to select the VSIX.  
  
## See Also  
 [VSIX Extension Schema 1.0 Reference](assetId:///76e410ec-b1fb-4652-ac98-4a4c52e09a2b)   
 [Anatomy of a VSIX Container](../vs140/Anatomy-of-a-VSIX-Package.md)   
 [How to: Deploy VSIX Content in an MSI](../vs140/Preparing-Extensions-for-Windows-Installer-Deployment.md)