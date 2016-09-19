---
title: "Registering Extensions of the .NET Framework"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: deee6f53-ea87-4b88-a120-bea589822e03
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Registering Extensions of the .NET Framework
You can develop an assembly that extends a specific version of the .NET Framework. To enable the assembly to appear in the Visual Studio **Add References** dialog box, you must add the folder that contains it to the system registry.  
  
 For example, assume that the Trey Research company has developed a library that extends the .NET Framework 4, and wants the library assemblies to appear in the **Add References** dialog box when a project targets the .NET Framework 4. Also assume that the assemblies are 32-bit assemblies running on a 32-bit computer or 64-bit assemblies running on a 64-bit computer, and that they will be installed in the C:\TreyResearch\Extensions4\ folder.  
  
 Register this folder by using this key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\\.NETFramework\v4.0.21006\AssemblyFoldersEx\TreyResearch\\. Give the key this default value: C:\TreyResearch\Extensions4.  
  
> [!NOTE]
>  The build number of the .NET Framework version may be different.  
  
 To register a 32-bit assembly on a 64-bit computer, use the Wow6432 node, for example: HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\\.NETFramework\v4.0.21006\AssemblyFoldersEx\TreyResearch\\.  
  
## See Also  
 [Visual Studio Integration (MSBuild)](../vs140/Visual-Studio-Integration--MSBuild-.md)