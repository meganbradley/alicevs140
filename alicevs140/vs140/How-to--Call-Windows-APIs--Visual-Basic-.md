---
title: "How to: Call Windows APIs (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 27d75f0a-54ab-4ee1-b91d-43513a19b12d
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Call Windows APIs (Visual Basic)
This example defines and calls the `MessageBox` function in user32.dll and then passes a string to it.  
  
## Example  
 [!CODE [VbVbalrInterop#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrInterop#1)]  
  
## Compiling the Code  
 This example requires:  
  
-   A reference to the <xref:System?qualifyHint=False> namespace.  
  
## Robust Programming  
 The following conditions may cause an exception:  
  
-   The method is not static, is abstract, or has been previously defined. The parent type is an interface, or the length of *name* or *dllName* is zero. (<xref:System.ArgumentException?qualifyHint=False>)  
  
-   The *name* or *dllName* is `Nothing`. (<xref:System.ArgumentNullException?qualifyHint=False>)  
  
-   The containing type has been previously created using `CreateType`. (<xref:System.InvalidOperationException?qualifyHint=False>)  
  
## See Also  
 [A Closer Look at Platform Invoke](assetId:///ba9dd55b-2eaa-45cd-8afd-75cb8d64d243)   
 [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f)   
 [Consuming Unmanaged DLL Functions](assetId:///eca7606e-ebfb-4f47-b8d9-289903fdc045)   
 [Defining a Method with Reflection Emit](assetId:///84fd3bf6-628f-41aa-83d9-b990cf926e81)   
 [Walkthrough: Calling Windows APIs](../Topic/Walkthrough:%20Calling%20Windows%20APIs%20\(Visual%20Basic\).md)   
 [COM Interop](../vs140/COM-Interop--Visual-Basic-.md)