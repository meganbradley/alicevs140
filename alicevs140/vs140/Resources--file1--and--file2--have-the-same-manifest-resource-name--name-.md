---
title: "Resources &#39;file1&#39; and &#39;file2&#39; have the same manifest resource name &#39;name&#39;"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 50d656ad-8557-4240-95b0-3f44b9c21da6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Resources &#39;file1&#39; and &#39;file2&#39; have the same manifest resource name &#39;name&#39;
The project system computed identical assembly resource names for two files whose `BuildAction` property is set to `EmbeddedResource` and that have a neutral culture. The build process will fail if this error occurs. For more information about the `BuildAction` property, see [File Properties](assetId:///013c4aed-08d6-4dce-a124-ca807ca08959).  
  
 Because [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] has no concept of folder-based namespaces, resource files names of:  
  
-   Proj1\FolderA\MyProj.bmp  
  
-   Proj1\FolderB\MyProj.bmp  
  
 will produce assembly manifest names of Proj1.MyProj.bmp for both files.  
  
 **To correct this error**  
  
-   To resolve this error, rename the affected resource files (*file1* and *file2*).  
  
## See Also  
 [NIB: Resource File Naming Conventions](assetId:///7b1a2cdf-6196-4034-8fc7-51a271842cc2)