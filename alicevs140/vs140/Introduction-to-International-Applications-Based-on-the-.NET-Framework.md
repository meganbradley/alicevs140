---
title: "Introduction to International Applications Based on the .NET Framework"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b0788993-e62d-4f68-8235-5f87b1d48525
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Introduction to International Applications Based on the .NET Framework
In [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], there are two parts to creating a world-ready application: globalization, the process of designing applications that can adapt to different cultures, and localization, the process of translating resources for a specific culture. For general information on designing applications for an international audience, see [Best Practices for Developing World-Ready Applications](assetId:///f08169c7-aad8-4ec3-9a21-9ebd3b89986c).  
  
 The [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] localization model consists of a main assembly that contains both the application code and the fallback resources — strings, images, and other objects for the language in which the application is originally developed. Each localized application will have satellite assemblies, or assemblies which contain only the localized resources. Because the main assembly always contains the fallback resources, if a resource is not found in the localized satellite assembly, the <xref:System.Resources.ResourceManager?qualifyHint=False> will attempt to load it in a hierarchical manner, eventually falling back to the resource in the main assembly. The resource fallback system is explained in greater detail in [Hierarchical Organization of Resources for Localization](../vs140/Hierarchical-Organization-of-Resources-for-Localization.md).  
  
 One localization resource you should consider using is the glossary for all Microsoft localized products. This CSV file contains over 12,000 English terms plus the translations of the terms in up to 59 different languages. The glossary is available for download on the [Microsoft Terminology Translations](http://go.microsoft.com/fwlink/?LinkId=128146) Web page.  
  
 The project system for Windows Forms applications can generate resource files for both the fallback and each desired additional UI culture. The fallback resource file is built into the main assembly, and the culture-specific resource files are then built into satellite assemblies, one for each UI culture. When you build a project, the resource files are compiled from the Visual Studio XML format (.resx) to an intermediate binary format (.resources), which are then embedded in satellite assemblies.  
  
 The project system for both Windows Forms and Web Forms allows you to build resource files using an Assembly Resource File template, access the resources, and build your project. Satellite assemblies will be created along with the main assembly.  
  
 When a localized application executes, its appearance is determined by two culture values. (A *culture* is a set of user preference information related to the user's language, environment, and cultural conventions.) The UI culture setting determines which resources will be loaded. The UI culture is set as `UICulture` in Web.config files and page directives, and <xref:System.Globalization.CultureInfo.CurrentUICulture?qualifyHint=False> in Visual Basic or Visual C# code. The culture setting determines formatting of values such as dates, numbers, currency, and so on. The culture is set as `Culture` in Web.config files and page directives, <xref:System.Globalization.CultureInfo.CurrentCulture?qualifyHint=False> in Visual Basic or Visual C# code.  
  
## See Also  
 <xref:System.Globalization?qualifyHint=False>   
 <xref:System.Resources?qualifyHint=False>   
 [Globalizing and Localizing Applications](../Topic/Globalizing%20and%20Localizing%20Applications.md)   
 [Security and Localized Satellite Assemblies](../vs140/Security-and-Localized-Satellite-Assemblies.md)