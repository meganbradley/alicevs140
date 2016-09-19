---
title: "Configuration name is not valid."
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aa439582-0863-41d3-825c-7c45b1773cde
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Configuration name is not valid.
This error generally occurs when the name entered for the build configuration includes illegal characters, such as <, >, &#124;, and *.  
  
### To correct this error  
  
1.  Check that the configuration name does not contain the following characters: <, >, *, &#124;, :, \\, /, &, %, ", ., #, ?, or a leading or trailing space. In addition, the configuration name cannot use names reserved for Windows or DOS, such as "nul", "aux", "con', "com#", "lpt#", and so on.  
  
2.  Re-type the name.  
  
## See Also  
 [Compiling and Building](../vs140/Compiling-and-Building-in-Visual-Studio.md)