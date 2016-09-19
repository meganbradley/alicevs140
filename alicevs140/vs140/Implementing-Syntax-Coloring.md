---
title: "Implementing Syntax Coloring"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 96e762ca-efd0-41e7-8958-fda4897c8c7a
caps.latest.revision: 22
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Implementing Syntax Coloring
When the language service provides syntax colorization, the parser converts a line of text into an array of colorable items and returns token types corresponding to these colorable items. The parser should return token types that belong to a list of colorable items. [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] displays each colorable item in the code window according to the attributes assigned by the colorizer object to the appropriate token type.  
  
 [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] does not specify a parser interface, and parser implementation is completely up to you. However, a default parser implementation is provided in the Visual Studio Language Package project. For managed code, the managed package framework (MPF) provides complete support for colorizing text.  
  
 Legacy language services are implemented as part of a VSPackage, but the newer way to implement language service features is to use MEF extensions. To find out more about the new way to implement syntax coloring, see [Walkthrough: Highlighting Text](../Topic/Walkthrough:%20Highlighting%20Text.md).  
  
> [!NOTE]
>  We recommend that you begin to use the new editor API as soon as possible. This will improve the performance of your language service and let you take advantage of new editor features.  
  
## Steps Followed by an Editor to Colorize Text  
  
1.  The editor gets the colorizer by calling the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageInfo.GetColorizer?qualifyHint=False> method on the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageInfo?qualifyHint=False> object.  
  
2.  The editor calls the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.GetStateMaintenanceFlag?qualifyHint=False> method to determine whether the colorizer needs the state of each line to be maintained outside the colorizer.  
  
3.  If the colorizer requires the state to be maintained outside the colorizer, the editor calls the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.GetStartState?qualifyHint=False> method to get the state of the first line.  
  
4.  For each line in the buffer, the editor calls the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.ColorizeLine?qualifyHint=False> method, which performs the following steps:  
  
    1.  The line of text is passed to a scanner to convert the text into tokens. Each token specifies the token text and the token type.  
  
    2.  The token type is converted into an index into a colorable items list.  
  
    3.  The token information is used to fill in an array such that each element of the array corresponds to a character in the line. The values stored in the array are the indexes into the colorable items list.  
  
    4.  The state at the end of the line is returned for each line.  
  
5.  If the colorizer requires the state to be maintained, the editor caches the state for that line.  
  
6.  The editor renders the line of text using the information returned from the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.ColorizeLine?qualifyHint=False> method. This requires the following steps:  
  
    1.  For each character in the line, get the colorable item index.  
  
    2.  If using the default colorable items, access the editor's colorable items list.  
  
    3.  Otherwise, call the language service's <xref:Microsoft.VisualStudio.TextManager.Interop.IVsProvideColorableItems.GetColorableItem?qualifyHint=False> method to obtain a colorable item.  
  
    4.  Use the information in the colorable item to render the text into the display.  
  
## Managed Package Framework Colorizer  
 The managed package framework (MPF) provides all the classes that are required to implement a colorizer. Your language service class should inherit the <xref:Microsoft.VisualStudio.Package.LanguageService?qualifyHint=False> class and implement the required methods. You must supply a scanner and parser by implementing the <xref:Microsoft.VisualStudio.Package.IScanner?qualifyHint=False> interface, and return an instance of that interface from the <xref:Microsoft.VisualStudio.Package.LanguageService.GetScanner?qualifyHint=False> method (one of the methods that must be implemented in the <xref:Microsoft.VisualStudio.Package.LanguageService?qualifyHint=False> class). For more information, see [Syntax Highlighting (Managed Package Framework)](../Topic/Syntax%20Colorizing%20in%20a%20Legacy%20Language%20Service.md).  
  
## See Also  
 [How to: Use Built-In Colorable Items](../Topic/How%20to:%20Use%20Built-In%20Colorable%20Items.md)   
 [Custom Colorable Items](../vs140/Custom-Colorable-Items.md)   
 [Developing a Language Service](../vs140/Developing-a-Legacy-Language-Service.md)   
 [Syntax Highlighting (Managed Package Framework)](../Topic/Syntax%20Colorizing%20in%20a%20Legacy%20Language%20Service.md)