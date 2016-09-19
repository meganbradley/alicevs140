---
title: "Determining Whether to Implement a Source Control VSPackage"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 60b3326e-e7e2-4729-95fc-b682e7ad5c99
caps.latest.revision: 26
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Determining Whether to Implement a Source Control VSPackage
This section elaborates the choices of source control plug-ins and source control VSPackages for extending source control solutions and gives broad guidelines about choosing a suitable integration path.  
  
## Small Source Control Solution with Limited Resources  
 If you have limited resources and cannot be burdened with the overhead of writing a source control package, you can create Source Control Plug-in API-based plug-ins. This allows you to work side by side with source control packages, and you can switch between source control plug-ins and packages on demand. For more information, see [Source-Control VSPackage Registration and Selection](../Topic/Registration%20and%20Selection%20\(Source%20Control%20VSPackage\).md).  
  
## Large Source Control Solution with a Rich Feature Set  
 If you want to implement a source control solution that provides a rich source control model that is not adequately captured by using the Source Control Plug-in API, you may consider a source control package as the integration path. This applies especially if you would rather replace the Source Control Adapter Package (which communicates with source control plug-ins and provides a basic source control UI) with your own so that you can handle the source control events in a custom manner. If you already have a satisfactory source control UI and want to preserve that experience in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], the source control package option lets you do just that. The source control package is not generic and is designed solely for use with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] IDE.  
  
 If you want to implement a source control solution that provides flexibility and richer control over the source control logic and UI, you may prefer the source control package integration route. You can:  
  
1.  Register your own source control VSPackage (see [Source-Control VSPackage Registration and Selection](../Topic/Registration%20and%20Selection%20\(Source%20Control%20VSPackage\).md)).  
  
2.  Replace the default source control UI with your custom UI (see [Custom UI (Source-Control VSPackage)](../vs140/Custom-User-Interface--Source-Control-VSPackage-.md)).  
  
3.  Specify glyphs to be used and handle Solution Explorer glyph events (see [Glyph Control (Source-Control VSPackage)](../Topic/Glyph%20Control%20\(Source%20Control%20VSPackage\).md)).  
  
4.  Handle Query Edit and Query Save events (see [Query Edit Query Save (Source-Control VSPackage)](../vs140/Query-Edit-Query-Save--Source-Control-VSPackage-.md)).  
  
## See Also  
 [Creating a Source Control Plug-in](../vs140/Creating-a-Source-Control-Plug-in.md)