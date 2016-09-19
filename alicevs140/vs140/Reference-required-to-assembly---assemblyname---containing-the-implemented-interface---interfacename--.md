---
title: "Reference required to assembly &#39;&lt;assemblyname&gt;&#39; containing the implemented interface &#39;&lt;interfacename&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b2dfb89d-7fde-4a8e-ba7f-fe1e59eabaca
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Reference required to assembly &#39;&lt;assemblyname&gt;&#39; containing the implemented interface &#39;&lt;interfacename&gt;&#39;
Reference required to assembly '<assemblyname\>' containing the implemented interface '<interfacename\>'. Add one to your project.  
  
 The interface is defined in a dynamic-link library (DLL) or assembly that is not directly referenced in your project. The [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler requires a reference to avoid ambiguity in case the interface is defined in more than one DLL or assembly.  
  
 **Error ID:** BC30009  
  
### To correct this error  
  
-   Include the name of the unreferenced DLL or assembly in your project references.  
  
## See Also  
 [NIB: Referencing Namespaces and Components](assetId:///568fa759-796b-44cd-bf5e-1cf8de6e38fd)   
 [Troubleshooting Broken References](../vs140/Troubleshooting-Broken-References.md)