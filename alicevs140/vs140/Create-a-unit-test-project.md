---
title: "Create a unit test project"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a608bfba-1a43-4a60-b73a-1fe53ef58098
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Create a unit test project
Unit tests often mirror the structure of the code under test. For example, a unit test project would be created for each code project in the product. The test project can be in the same solution as the production code, or it can be in a separate solution. You can have multiple unit test projects in a solution.  
  
> [!NOTE]
>  The location of unit tests for native code and the test project structure can be different than the structure that is described in this topic. For more information, see [Unit Testing Existing C++ Applications with Test Explorer](../vs140/Unit-testing-existing-C---applications-with-Test-Explorer.md).  
  
## To create a unit test project:  
  
1.  On the **File** menu, choose **New** and then choose **Project** (Keyboard Ctrl + Shift + N).  
  
2.  In the New Project dialog box, expand the **Installed** node, choose the language that you want to use for your test project, and then choose **Test**.  
  
3.  To use one of the Microsoft unit test frameworks, choose **Unit Test Project** from the list of project templates. Otherwise, choose the project template of the unit test framework that you want to use. To test the Accounts project of our example, you would name the project AccountsTests.  
  
4.  In your unit test project, add a reference to the code under test.  Here’s how to create the reference to a code project in the same solution:  
  
    1.  Select the project in Solution Explorer.  
  
    2.  On the **Project** menu, choose **Add Reference...**.  
  
    3.  In the Reference Manager dialog box, open the **Solution** node and choose **Projects**. Check the code project name and close the dialog box.  
  
5.  If the code that you want to test is in another location, see [Managing Project References](../Topic/Managing%20references%20in%20a%20project.md) for information about adding references.  
  
## Next steps  
 **Writing unit tests**  
  
 See one of the following sections:  
  
-   [Writing unit tests for .NET with the Microsoft Unit Test Framework for Managed Code](../vs140/Writing-Unit-Tests-for-the-.NET-Framework-with-the-Microsoft-Unit-Test-Framework-for-Managed-Code.md)  
  
-   [Writing unit tests for C++ with the Microsoft Unit Testing Framework for C++](../vs140/Writing-Unit-tests-for-C-C---with-the-Microsoft-Unit-Testing-Framework-for-C--.md)  
  
 **Running unit tests**  
  
 [Running Unit Tests with Unit Test Explorer](../Topic/Run%20unit%20tests%20with%20Test%20Explorer.md)