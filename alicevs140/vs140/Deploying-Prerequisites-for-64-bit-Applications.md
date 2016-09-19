---
title: "Deploying Prerequisites for 64-bit Applications"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-deployment
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 87399e20-5510-41e4-b5b7-4a87c5773f21
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Deploying Prerequisites for 64-bit Applications
ClickOnce deployment supports the installation of applications on 64-bit platforms. The target platforms are **x86** for 32-bit platforms, **x64** for machines supporting the AMD64 and EM64T instruction sets, and **Itanium** for the 64-bit Itanium processor.  
  
## Prerequisites  
 The following table lists the redistributables that you can use as prerequisites for your 64-bit application's installation.  
  
 If you select a prerequisite that does not have 64-bit components, you may see a warning stating that the selected packages are not available for the 64-bit platform.  
  
|Redistributable|x64 support|IA64 support|  
|---------------------|-----------------|------------------|  
|[!INCLUDE[vsto_runtime](../vs140/includes/vsto_runtime_md.md)]|Yes|No|  
|Visual C++ 2010 Runtime Libraries (IA64)|No|Yes|  
|Visual C++ 2010 Runtime Libriaries (x64)|Yes|No|  
|Microsoft .NET Framework 4 (x86 and x64)|Yes||  
|Microsoft .NET Framework 4 Client Profile (x86 and x64)|Yes||  
  
## See Also  
 [Deploying Applications and Components](../vs140/Deploying-Applications--Services--and-Components.md)   
 [How to: Install Prerequisites with a ClickOnce Application](../vs140/How-to--Install-Prerequisites-with-a-ClickOnce-Application.md)   
 [64-bit Applications](assetId:///fd4026bc-2c3d-4b27-86dc-ec5e96018181)