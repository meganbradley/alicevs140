---
title: "Visual Studio Template Schema Reference"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6f74a2d5-3811-43d6-8b10-eb5823ad8995
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Visual Studio Template Schema Reference
This section contains information about XML elements in .vstemplate files, which are files that store metadata for project templates, item templates, and Starter Kits.  
  
 You can use vstemplate.xsd to validate custom .vstemplate files. This file is available at ..\\*Visual Studio installation folder*\Xml\Schemas\1033\vstemplate.xsd.  
  
|Element|Child Elements|Attributes|  
|-------------|--------------------|----------------|  
|[AppliesTo](../vs140/AppliesTo-Element--Visual-Studio-Templates-.md)|None|None|  
|[Assembly (Template)](../vs140/Assembly-Element--Visual-Studio-Templates-.md)|--|--|  
|[Assembly (Wizard Extension)](../vs140/Assembly-Element--Visual-Studio-Template-Wizard-Extension-.md)|--|--|  
|[BuildProjectOnload](../vs140/BuildProjectOnload-Element--Visual-Studio-Templates-.md)|--|--|  
|[CreateInPlace](../vs140/CreateInPlace--Visual-Studio-Templates-.md)|--|--|  
|[CreateNewFolder](../vs140/CreateNewFolder-Element--Visual-Studio-Templates-.md)|--|--|  
|[CustomDataSignature](../vs140/CustomDataSignature-Element--Visual-Studio-Templates-.md)|--|--|  
|[CustomParameter](../vs140/CustomParameter-Element--Visual-Studio-Templates-.md)|--|Name<br /><br /> Value|  
|[CustomParameters](../vs140/CustomParameters-Element--Visual-Studio-Templates-.md)|CustomParameter|--|  
|[DefaultName](../vs140/DefaultName-Element--Visual-Studio-Templates-.md)|--|--|  
|[Description](../vs140/Description-Element--Visual-Studio-Templates-.md)|--|Package<br /><br /> ID|  
|[EnableEditOfLocationField](../vs140/EnableEditOfLocationField-Element--Visual-Studio-Templates-.md)|--|--|  
|[EnableLocationBrowseButton](../vs140/EnableLocationBrowseButton-Element--Visual-Studio-Templates-.md)|--|--|  
|[Folder](../vs140/Folder-Element--Visual-Studio-Project-Templates-.md)|ProjectItem<br /><br /> Folder|Name|  
||[deprecated]|--|  
|[FullClassName](../vs140/FullClassName-Element--Visual-Studio-Template-Wizard-Extension-.md)|--|--|  
|[Hidden](../vs140/Hidden-Element--Visual-Studio-Templates-.md)|--|--|  
|[Icon](../vs140/Icon-Element--Visual-Studio-Templates-.md)|--|Package<br /><br /> ID|  
|[LocationField](../vs140/LocationField-Element--Visual-Studio-Project-Templates-.md)|--|--|  
|[LocationFieldMRUPrefix](../vs140/LocationFieldMRUPrefix-Element--Visual-Studio-Templates-.md)|--|--|  
|[MaxFrameworkVersion](../vs140/MaxFrameworkVersion-Element--Visual-Studio-Templates-.md)|--|--|  
|[Name](../vs140/Name-Element--Visual-Studio-Templates-.md)|--|Package<br /><br /> ID|  
|[NumberOfParentCategoriesToRollUp](../vs140/NumberOfParentCategoriesToRollUp--Visual-Studio-Templates-.md)|--|--|  
|[PreviewImage](../vs140/PreviewImage-Element--Visual-Studio-Templates-.md)|--|--|  
|[Project](../vs140/Project-Element--Visual-Studio-Templates-.md)|Folder<br /><br /> ProjectItem|File<br /><br /> TargetFileName<br /><br /> ReplaceParameters|  
|[ProjectCollection](../vs140/ProjectCollection-Element--Visual-Studio-Templates-.md)|ProjectTemplateLink<br /><br /> SolutionFolder|--|  
|[ProjectItem (Item Templates)](../vs140/ProjectItem-Element--Visual-Studio-Item-Templates-.md)|--|SubType<br /><br /> CustomTool<br /><br /> ItemType<br /><br /> ReplaceParameters<br /><br /> TargetFileName|  
|[ProjectItem (Project Templates)](../vs140/ProjectItem-Element--Visual-Studio-Project-Templates-.md)|--|TargetFileName<br /><br /> ReplaceParameters<br /><br /> OpenInEditor<br /><br /> OpenOrder<br /><br /> OpenInWebBrowser<br /><br /> OpenInHelpBrowser|  
|[ProjectSubType](../vs140/ProjectSubType-Element--Visual-Studio-Templates-.md)|--|--|  
|[ProjectTemplateLink](../vs140/ProjectTemplateLink-Element--Visual-Studio-Templates-.md)|--|ProjectName|  
|[ProjectType](../vs140/ProjectType-Element--Visual-Studio-Templates-.md)|--|--|  
|[PromptForSaveOnCreation](../vs140/PromptForSaveOnCreation-Element--Visual-Studio-Templates-.md)|--|--|  
|[ProvideDefaultName](../vs140/ProvideDefaultName-Element--Visual-Studio-Templates-.md)|--|--|  
|[Reference](../vs140/Reference-Element--Visual-Studio-Templates-.md)|Assembly|--|  
|[References](../vs140/References-Element--Visual-Studio-Templates-.md)|Reference|--|  
|[RequiredFrameworkVersion](../vs140/RequiredFrameworkVersion-Element--Visual-Studio-Templates-.md)|--|--|  
|[RequiredPlatformVersion](../vs140/RequiredPlatformVersion-Element--Visual-Studio-Templates-.md)|--|Version|  
|[SDKReference](72c8b352-0b7a-42b3-ba5d-2a2d1e90c3)|--|Package|  
|[ShowByDefault](../vs140/ShowByDefault--Visual-Studio-Templates-.md)|--|--|  
|[SolutionFolder](../vs140/SolutionFolder-Element--Visual-Studio-Templates-.md)|ProjectTemplateLink<br /><br /> SolutionFolder|Name|  
|[SortOrder](../vs140/SortOrder-Element--Visual-Studio-Templates-.md)|--|--|  
|[SupportsCodeSeparation](../vs140/SupportsCodeSeparation-Element--Visual-Studio-Templates-.md)|--|--|  
|[SupportsLanguageDropDown](../vs140/SupportsLanguageDropDown-Element--Visual-Studio-Templates-.md)|--|--|  
|[SupportsMasterPage](../vs140/SupportsMasterPage-Element--Visual-Studio-Templates-.md)|--|--|  
|[TargetPlatformName](../vs140/TargetPlatformName-Element--Visual-Studio-Templates-.md)|RequiredPlatformVersion|--|  
|[TemplateContent](../vs140/TemplateContent-Element--Visual-Studio-Templates-.md)|ProjectCollection<br /><br /> Project<br /><br /> References<br /><br /> ProjectItem<br /><br /> CustomParameters|[BuildOnLoad](../vs140/BuildProjectOnLoad--Visual-Studio-Templates-.md)|  
|[TemplateData](../vs140/TemplateData-Element--Visual-Studio-Templates-.md)|Name<br /><br /> Description<br /><br /> Icon<br /><br /> PreviewImage<br /><br /> ProjectType<br /><br /> ProjectSubType<br /><br /> TemplateID<br /><br /> TemplateGroupID<br /><br /> SortOrder<br /><br /> CreateNewFolder<br /><br /> DefaultName<br /><br /> ProvideDefaultName<br /><br /> PromptForSaveOnCreation<br /><br /> EnableLocationBrowseButton<br /><br /> EnableEditOfLocationField<br /><br /> Hidden<br /><br /> DisplayInParentCategories<br /><br /> LocationFieldMRUPrefix<br /><br /> NumberOfParentCategoriesToRollUp<br /><br /> CreateInPlace<br /><br /> BuildOnLoad<br /><br /> BuildProjectOnload<br /><br /> ShowByDefault<br /><br /> LocationField<br /><br /> SupportsMasterPage<br /><br /> SupportsCodeSeparation<br /><br /> SupportsLanguageDropDown<br /><br /> RequiredFrameworkVersion<br /><br /> FrameworkVersion<br /><br /> MaxFrameworkVersion<br /><br /> CustomDataSignature<br /><br /> TargetPlatformName|--|  
|[TemplateGroupID](../vs140/TemplateGroupID-Element--Visual-Studio-Templates-.md)|--|--|  
|[TemplateID](../vs140/TemplateID-Element--Visual-Studio-Templates-.md)|--|--|  
|[VSTemplate](../vs140/VSTemplate-Element--Visual-Studio-Templates-.md)|TemplateData<br /><br /> TemplateContent<br /><br /> WizardExtension<br /><br /> WizardData|Type<br /><br /> Version|  
|[WizardData](../vs140/WizardData-Element--Visual-Studio-Templates-.md)|--|Name|  
|[WizardExtension](../vs140/WizardExtension-Element--Visual-Studio-Templates-.md)|Assembly<br /><br /> FullClassName|--|  
  
## See Also  
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)   
 [How to: Create Starter Kits](../vs140/How-to--Create-Starter-Kits.md)