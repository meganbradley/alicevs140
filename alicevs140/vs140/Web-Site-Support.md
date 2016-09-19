---
title: "Web Site Support"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ce9f4266-bb64-4c09-be88-4bd6413f60d0
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Web Site Support
A Web site project system is a project system that creates Web projects. Web projects in turn create Web applications. A Web site project generates one executable file for each Web page that has associated code. Additional executable files are generated from the source code files in the /App_Code folder.  
  
 Web site project systems are created by adding templates and registration attributes to an existing project system. One of these attributes selects the IntelliSense provider for the language. The IntelliSense provider implementation handles references and calls the language compiler when a smart Web page that is not cached is requested.  
  
 The language compiler used to compile Web pages must be registered with [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)]. You can use the [<compiler\> element](assetId:///7a151659-b803-4c27-b5ce-1c4aa0d5a823) in a Web.config file to register the compiler, as in the following example:  
  
```  
<system.codedom>  <compilers>    <compiler language="py;IronPython" extension=".py"       type="IronPython.CodeDom.PythonProvider, IronPython,       Version=1.0.2391.18146, Culture=neutral,       PublicKeyToken=b03f5f7f11d50a3a" />  </compilers></system.codedom>  
```  
  
## In This Section  
 [Web Site Support Templates](../vs140/Web-Site-Support-Templates.md)  
 Lists the templates that you can use to create new Web site projects and associated items.  
  
 [Web Site Support Registration Attributes](../Topic/Web%20Site%20Support%20Attributes.md)  
 Presents the registration attributes that connect a Web site project to [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] and [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)].  
  
## Related Sections  
 [Web Projects](../vs140/Web-Projects.md)  
 Presents an overview of the two kinds of Web projects, Web site projects and Web application projects.