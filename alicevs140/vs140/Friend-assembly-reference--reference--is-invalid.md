---
title: "Friend assembly reference &lt;reference&gt; is invalid"
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
ms.assetid: 6540c1d0-bb19-4051-a579-2e4f9094585e
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Friend assembly reference &lt;reference&gt; is invalid
Friend assembly reference <reference\> is invalid. Strong-name signed assemblies must specify a public key in their InternalsVisibleTo declarations.  
  
 The assembly name passed to the <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute?qualifyHint=False> attribute constructor identifies a strong-named assembly, but it does not include a `PublicKey` attribute.  
  
 **Error ID:** BC31535  
  
### To correct this error  
  
1.  Determine the public key for the strong-named friend assembly. Include the public key as part of the assembly name passed to the <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute?qualifyHint=False> attribute constructor by using the `PublicKey` attribute.  
  
## See Also  
 <xref:System.Reflection.AssemblyName?qualifyHint=False>   
 [Friend Assemblies (C# and Visual Basic)](../vs140/Friend-Assemblies--C#-and-Visual-Basic-.md)   
 [How to: Create Signed Friend Assemblies](../vs140/How-to--Create-Signed-Friend-Assemblies--C#-and-Visual-Basic-.md)