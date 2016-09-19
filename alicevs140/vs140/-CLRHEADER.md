---
title: "-CLRHEADER"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: /CLRHEADER
ms.assetid: cf73424f-4541-47e2-b94e-69b95266ef2a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -CLRHEADER
```  
/CLRHEADER file  
```  
  
## Remarks  
 where:  
  
 `file`  
 An image file built with [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
## Remarks  
 CLRHEADER displays information about the .NET headers used in any managed program. The output shows the location and size, in bytes, of the .NET header and sections in the header.  
  
 Only the [/HEADERS](../vs140/-HEADERS.md) DUMPBIN option is available for use on files produced with the [/GL](../Topic/-GL%20\(Whole%20Program%20Optimization\).md) compiler option.  
  
 When /CLRHEADER is used on a file that was compiled with /clr, there will be a **clr Header:** section in the dumpbin output.  The value of **flags** indicates which /clr option was used:  
  
-   0  -- /clr (image may contain native code).  
  
-   1 -- /clr:safe (image is MSIL only, able to run on any CLR platform, and possibly verifiable).  
  
-   3 -- /clr:pure (image is MSIL only, but only able to run on x86 platforms).  
  
 You can also programmatically check if an image was built for the common language runtime.  For more information, see [How to: Determine if Image is Native or CLR](../vs140/How-to--Determine-if-an-Image-is-Native-or-CLR.md).  
  
## See Also  
 [DUMPBIN Options](../vs140/DUMPBIN-Options.md)