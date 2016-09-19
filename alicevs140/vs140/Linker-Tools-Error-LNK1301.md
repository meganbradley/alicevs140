---
title: "Linker Tools Error LNK1301"
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
ms.topic: error-reference
ms.assetid: 760da428-7182-4b25-b20a-de90d4b9a9cd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1301
LTCG clr modules found, incompatible with /LTCG:parameter  
  
 A module compiled with /clr and /GL was passed to the linker along with one of the profile guided optimizations (PGO) parameters of /LTCG.  
  
 Profile guided optimizations are not supported for /clr modules.  
  
 For more information, see:  
  
-   [/GL (Whole Program Optimization)](../Topic/-GL%20\(Whole%20Program%20Optimization\).md)  
  
-   [/LTCG (Link-time Code Generation)](../vs140/-LTCG--Link-time-Code-Generation-.md)  
  
-   [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md)  
  
-   [Profile-Guided Optimizations](../vs140/Profile-Guided-Optimizations.md)  
  
### To correct this error  
  
1.  Do not compile with /clr or do not link with one of the PGO parameters to /LTCG.  
  
## Example  
 The following sample generates LNK1301:  
  
```  
// LNK1301.cpp  
// compile with: /clr /GL /link /LTCG:PGI LNK1301.obj  
// LNK1301 expected  
class MyClass {  
public:  
   int i;  
};  
```