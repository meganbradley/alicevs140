---
title: "Implementing Custom Categories and Display Items"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 99311a93-d642-4344-bbf9-ff6e7fa5bf7f
caps.latest.revision: 27
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Implementing Custom Categories and Display Items
A VSPackage can provide control of the fonts and colors of its text to the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] integrated development environment (IDE) through custom categories and display items.  
  
 Custom categories and display items are on the **Fonts and Colors** property page. To open the **Fonts and Colors** property page, on the **Tools** menu, click **Options**. Expand **Environment** and then click **Fonts and Colors**.  
  
 When using this mechanism, VSPackages must implement the <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider?qualifyHint=False> interface and its associated interfaces.  
  
 In principle, this mechanism can be used to modify all existing **Display items** and the **Categories** that contain them. However, it should not be used to modify the **Text EditorCategory** or its **Display items**. For more information, see [Core Editor Font and Color Mechanism](../Topic/Font%20and%20Color%20Overview.md).  
  
 To implement custom **Categories** or **Display items**, a VSPackage must:  
  
-   Create or identify categories in the registry.  
  
     The IDE's implementation of the **Fonts and Colors** property page uses this information to correctly query for the service supporting a given category.  
  
-   Create or identify groups (optional) in the registry.  
  
     It may be useful to define a group, which represents the union of two or more categories. If a group is defined, the IDE automatically merges subcategories and distributes display items within the group.  
  
-   Implement IDE support.  
  
-   Handle font and color changes.  
  
 For information, see [How to: Persist Default Font and Color Settings](../vs140/Accessing-Stored-Font-and-Color-Settings.md).  
  
## To create or identify categories  
  
-   Construct a special type of category registry entry under [HKLM\SOFTWARE\Microsoft \Visual Studio\\*<Visual Studio version\>*\FontAndColors\\`<Category>`]  
  
     *<Category\>* is the non-localized name of the category.  
  
-   Populate the registry with two values:  
  
    |Name|Type|Data|Description|  
    |----------|----------|----------|-----------------|  
    |Category|REG_SZ|GUID|A GUID created to identify the category.|  
    |Package|REG_SZ|GUID|The GUID of the VSPackage service that supports the category.|  
  
 The service specified in the registry must provide an implementation of <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults?qualifyHint=False> for the corresponding category.  
  
## To Create or Identify Groups  
  
-   Construct a special type of category registry entry under [HKLM\SOFTWARE\Microsoft \Visual Studio\\*<Visual Studio version\>*\FontAndColors\\*<group\>*]  
  
     *<group\>* is the non-localized name of the group.  
  
-   Populate the registry with two values:  
  
    |Name|Type|Data|Description|  
    |----------|----------|----------|-----------------|  
    |Category|REG_SZ|GUID|A GUID created to identify the group.|  
    |Package|REG_SZ|GUID|The GUID of the service that supports the category.|  
  
 The service specified in the registry must provide an implementation of `T:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorGroup` for the corresponding group.  
  
## To Implement IDE Support  
  
-   Implement <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider.GetObject?qualifyHint=False>, which returns either an <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults?qualifyHint=False> interface or an `T:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorGroup` interface to the IDE for each **Category** or group GUID supplied.  
  
-   For every **Category** it supports, a VSPackage implements a separate instance of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults?qualifyHint=False> interface.  
  
-   The methods implemented through <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults?qualifyHint=False> must provide the IDE with:  
  
    -   Lists of **Display items** in the **Category.**  
  
    -   Localizable names for **Display items**.  
  
    -   Display information for each member of **Category**.  
  
    > [!NOTE]
    >  Every **Category** must contain at least one **Display item**.  
  
-   The IDE uses the `T:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorGroup` interface to define a union of several categories.  
  
     Its implementation provides the IDE with:  
  
    -   A list of the **Categories** that comprise a given group.  
  
    -   Access to instances of <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults?qualifyHint=False> supporting each **Category** within the group.  
  
    -   Localizable group names.  
  
-   Updating the IDE:  
  
     The IDE caches information about **Font and Color** settings. Therefore, after any modification of the IDE **Font and Color** configuration, it is advisable to make sure that the cache is up-to-date.  
  
 Updating the cache is done through the <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorCacheManager?qualifyHint=False> interface and can be performed globally or just on selected items.  
  
## To Handle Font and Color Changes  
 To properly support the colorization of text that a VSPackage displays, the colorization service supporting the VSPackage must respond to the user-initiated changes made through the **Fonts and Colors** properties page. A VSPackage does this by:  
  
-   Handling IDE-generated events by implementing the <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorEvents?qualifyHint=False> interface.  
  
     The IDE calls the appropriate method following user modifications of the **Fonts and Colors** page. For example, it calls the <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorEvents.OnFontChanged?qualifyHint=False> method if a new font is selected.  
  
     -or-  
  
-   Polling the IDE for changes.  
  
     This can be done through the system-implemented <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorStorage?qualifyHint=False> interface. Although primarily for support of persistence, the <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorStorage.GetItem?qualifyHint=False> method can be used to obtain font and color information for **Display items**. For more information, see [How to: Persist Default Font and Color Settings](../vs140/Accessing-Stored-Font-and-Color-Settings.md).  
  
    > [!NOTE]
    >  To ensure that the results obtained by polling are correct, it may be useful to use the <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorCacheManager?qualifyHint=False> interface to determine if a cache flush and update are needed prior to calling the retrieval methods of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorStorage?qualifyHint=False> interface.  
  
## See Also  
 <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider.QueryService?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorEvents?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorStorage?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorGroup?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider?qualifyHint=False>   
 [How to: Colorize Using the Default Font And Color Mechanism](../Topic/Getting%20Font%20and%20Color%20Information%20for%20Text%20Colorization.md)   
 [How to: Persist Default Font and Color Settings](../vs140/Accessing-Stored-Font-and-Color-Settings.md)   
 [How to: Use Built-in Categories and Display Items](../Topic/How%20to:%20Access%20the%20Built-in%20Fonts%20and%20Color%20Scheme.md)   
 [Core Editor Font and Color Mechanism](../Topic/Font%20and%20Color%20Overview.md)