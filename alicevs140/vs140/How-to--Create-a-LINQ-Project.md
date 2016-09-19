---
title: "How to: Create a LINQ Project"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a929e653-09a3-44be-881f-68ca33f192b2
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a LINQ Project
The .NET Framework version 3.5 introduces namespaces and references that are required for basic [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] functionality in Visual C# and Visual Basic. Just create a new project and you can start writing [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] queries against object collections. Visual Basic additionally provides a reference and imported namespace for [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] functionality. In Visual C# these must be added manually.  
  
 To use [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] or [!INCLUDE[linq_dataset](../vs140/includes/linq_dataset_md.md)] in either language, you must manually add namespaces and references as described in the following sections.  
  
 If you are upgrading a project that you created by using an earlier version of Visual Studio, you may have to supply these or other [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)]-related references manually and also manually set the project to target .NET Framework version 3.5.  
  
> [!NOTE]
>  If you are building at a command prompt, you must manually reference the [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] -related DLLs in *drive*:\Program Files\Reference Assemblies\Microsoft\Framework\v3.5.  
  
## Procedures to add LINQ Namespaces and References  
  
#### To target the .NET Framework version 3.5  
  
1.  In Visual Studio, open a Visual Basic or C# project that was created in Visual Studio 2005 and follow the prompts to convert it to a Visual Studio 2008 or a Visual Studio 2010 project.  
  
2.  For a C# project, click the **Project** menu, and then click **Properties**.  
  
    1.  In the **Application** property page, select **.NET Framework 3.5** in the **Target Framework** drop-down list.  
  
3.  For a Visual Basic project, click the **Project** menu, and then click **Properties**.  
  
     In the **Compile** property page, click **Advanced Compile Options** and then select **.NET Framework 3.5** in the **Target Framework (all configurations)** drop-down list.  
  
#### To enable basic LINQ functionality  
  
1.  In a Visual Basic or C# project, click the **Project** menu, and then click **Add Reference**.  
  
2.  In the **Add Reference** dialog box, click the **.NET** tab, scroll to System.Core.dll, and then click it. Click **OK**.  
  
3.  Add a `using` directive or `Imports` statement for <xref:System.Linq?qualifyHint=False> to your source code file or project.  
  
     For more information, see [using Directive (C# Reference)](../Topic/using%20Directive%20\(C%23%20Reference\).md) or [How to: Add or Remove Imported Namespaces (Visual Basic)](../vs140/How-to--Add-or-Remove-Imported-Namespaces--Visual-Basic-.md).  
  
#### To enable advanced LINQ functionality with expression trees  
  
1.  If you already have a reference to System.Core.dll, add a `using` directive or `Imports` statement for <xref:System.Linq.Expressions?qualifyHint=False>.  
  
     For more information, see [Expression Trees](../vs140/Expression-Trees--C#-and-Visual-Basic-.md).  
  
#### To use LINQ to XML  
  
1.  If necessary, follow the steps earlier in this topic to add a reference to System.Core.dll and a `using` directive or `Imports` statement for System.Linq.  
  
2.  Add a reference to System.Xml.Linq.  
  
3.  Add a `using` directive or `Imports` statement for System.Xml.Linq.  
  
    > [!NOTE]
    >  By default, this functionality is provided for Visual Basic projects.  
    >   
    >  For more information, see [LINQ to XML](../vs140/LINQ-to-XML.md).  
  
#### To use LINQ to SQL  
  
1.  If necessary, follow the steps earlier in this topic to add a reference to System.Core.dll and a `using` directive or `Imports` statement for System.Linq.  
  
2.  Add a reference to System.Data.Linq.  
  
3.  Add a `using` directive or `Imports` statement for <xref:System.Data.Linq?qualifyHint=False> or one of the other System.Data.Linq namespaces depending on the requirements of your particular project.  
  
     For more information, see [LINQ to SQL](assetId:///73d13345-eece-471a-af40-4cc7a2f11655).  
  
#### To use LINQ to Dataset  
  
1.  If necessary, follow the steps earlier in this topic to add a reference to System.Core.dll and a `using` directive or `Imports` statement for System.Linq.  
  
2.  Add a reference to System.Data.DataSetExtensions.dll for [!INCLUDE[linq_dataset](../vs140/includes/linq_dataset_md.md)] functionality. Add a reference to System.Data.dll if it does not already exist.  
  
3.  Add a `using` directive or `Imports` statement for System.Data, and optionally for System.Data.Common, System.Data.SqlClient, depending on how you connect to the database.  
  
     For more information, see [LINQ to DataSet](assetId:///743e3755-3ecb-45a2-8d9b-9ed41f0dcf17).  
  
## See Also  
 [Language-Integrated Query (LINQ)](../vs140/LINQ--Language-Integrated-Query-.md)   
 [using Directive (C# Reference)](../Topic/using%20Directive%20\(C%23%20Reference\).md)