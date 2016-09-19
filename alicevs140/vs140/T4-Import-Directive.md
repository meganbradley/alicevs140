---
title: "T4 Import Directive"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 713ca975-b9aa-4210-bf6d-b7660f5b193b
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# T4 Import Directive
In the code blocks of a [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] T4 text template, the `import` directive allows you to refer to elements in another namespace without providing a fully-qualified name. It is the equivalent of `using` in C# or `imports` in [!INCLUDE[vb_current_short](../vs140/includes/vb_current_short_md.md)].  
  
 For a general overview of writing T4 text templates, see [Writing a Text Template](../vs140/Writing-a-T4-Text-Template.md).  
  
## Using the Import Directive  
  
```  
<#@ import namespace="namespace" #>  
```  
  
 In this example, template code can omit an explicit namespace for members of System.IO:  
  
```  
<#@ import namespace="System.IO" #>  
<#   
   string fileContent = File.ReadAllText("C:\x.txt"); // System.IO.File  
#>   
The file contains: <#=  fileContent #>  
```  
  
## Standard Imports  
 The following namespace is imported automatically, so that you do not need to write an import directive for it:  
  
-   `System`  
  
 In addition, if you use a custom directive, the directive processor might import some namespaces automatically.  
  
 For example, if you write templates for a domain-specific language (DSL), you do not need to write import directives for the following namespaces:  
  
-   `Microsoft.VisualStudio.Modeling`  
  
-   Your DSL’s namespace  
  
## See Also  
 [Assembly Directive](../vs140/T4-Assembly-Directive.md)