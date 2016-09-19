---
title: "Implementing class &#39;&lt;classname&gt;&#39; for interface &lt;interfacename&gt; cannot be found"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 262cb67e-2930-4a4a-a63e-bb2e201b3b93
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Implementing class &#39;&lt;classname&gt;&#39; for interface &lt;interfacename&gt; cannot be found
An implementing class in the interop assembly is not available.  
  
 **Error ID:** BC31094  
  
### To correct this error  
  
1.  Verify that the type library for the COM object is valid.  
  
2.  Use the Type Library Importer (Tlbimp.exe) to manually create an interop assembly, and then add a reference to that interop assembly from your project.  
  
## See Also  
 [Implements Statement](../vs140/Implements-Statement.md)   
 [COM Interop](../vs140/COM-Interop--Visual-Basic-.md)   
 [Type Library Importer (Tlbimp.exe)](assetId:///ec0a8d63-11b3-4acd-b398-da1e37e97382)