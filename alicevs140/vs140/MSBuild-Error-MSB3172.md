---
title: "MSBuild Error MSB3172"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aa7291db-1f36-41e7-a510-90cd4daaa89d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3172
**MSB3172: Unable to read manifest '<file\>'. '<error\>'**  
  
 This error is generated when the build process encounters a general problem reading a manifest file. The error message contains the file name followed by more detailed information about what went wrong.  
  
 You might have added an assembly or a manifest file as a content file. You should use the **Add Reference** command instead of **Add File** so that the dependent assembly is properly referenced by the project system. More sophisticated projects commonly mark the .exe.manifest in the bin folder as a project file, but you should avoid doing so. The hidden app.manifest file becomes the .exe.manifest file and can be edited manually for advanced scenarios.  
  
## See Also  
 [<PackageFiles\> Element (ClickOnce Bootstrapper)](../vs140/-PackageFiles--Element--Bootstrapper-.md)