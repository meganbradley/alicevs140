---
title: "How to: Display an Item List Separated with Commas"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3cae844c-7c6d-4144-82dc-efad10ba458f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Display an Item List Separated with Commas
When you work with item lists in [!INCLUDE[vstecmsbuildengine](../vs140/includes/vstecmsbuildengine_md.md)] ([!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)]), it is sometimes useful to display the contents of those item lists in a way that is easy to read. Or, you might have a task that takes a list of items separated with a special separator string. In both of these cases, you can specify a separator string for an item list.  
  
## Separating Items in a List with Commas  
 By default, [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] uses semicolons to separate items in a list. For example, consider a `Message` element with the following value:  
  
 `<Message Text="This is my list of TXT files: @(TXTFile)"/>`  
  
 When the `@(TXTFile)` item list contains the items App1.txt, App2.txt, and App3.txt, the message is:  
  
 `This is my list of TXT files: App1.txt;App2.txt;App3.txt`  
  
 If you want to change the default behavior, you can specify your own separator. The syntax for specifying an item list separator is:  
  
 `@(ItemListName, '<separator>')`  
  
 The separator can be either a single character or a string and must be enclosed in single quotes.  
  
#### To insert a comma and a space between items  
  
-   Use item notation similar to the following:  
  
     `@(TXTFile, ', ')`  
  
## Example  
 In this example, [Exec](../Topic/Exec%20Task.md) task runs the findstr tool to find specified text strings in the file, Phrases.txt. In the findstr command, literal search strings are indicated by the **/c:** switch, so the item separator, `/c:` is inserted between items in the `@(Phrase)` item list.  
  
 For this example, the equivalent command-line command is:  
  
 `findstr /i /c:hello /c:world /c:msbuild phrases.txt`  
  
```  
<Project DefaultTargets = "Find"  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003" >  
  
    <ItemGroup>  
        <Phrase Include="hello"/>  
        <Phrase Include="world"/>  
        <Phrase Include="msbuild"/>  
    </ItemGroup>  
  
    <Target Name = "Find">  
        <!-- Find some strings in a file -->  
        <Exec Command="findstr /i /c:@(Phrase, ' /c:') phrases.txt"/>  
    </Target>  
</Project>  
```  
  
## See Also  
 [MSBuild Reference](../Topic/MSBuild%20Reference.md)   
 [MSBuild Items](../vs140/MSBuild-Items.md)