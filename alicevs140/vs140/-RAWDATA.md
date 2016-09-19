---
title: "-RAWDATA"
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
H1: /RAWDATA
ms.assetid: 41cba845-5e1f-415e-9fe4-604a52235983
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -RAWDATA
```  
/RAWDATA[:{1|2|4|8|NONE[,number]]  
```  
  
## Remarks  
 This option displays the raw contents of each section in the file. The arguments control the format of the display, as shown below:  
  
|Argument|Result|  
|--------------|------------|  
|1|The default. Contents are displayed in hexadecimal bytes, and also as ASCII characters if they have a printed representation.|  
|2|Contents are displayed as hexadecimal 2-byte values.|  
|4|Contents are displayed as hexadecimal 4-byte values.|  
|8|Contents are displayed as hexadecimal 8-byte values.|  
|NONE|Raw data is suppressed. This argument is useful to control the output of /ALL.|  
|*Number*|Displayed lines are set to a width that holds `number` values per line.|  
  
 Only the [/HEADERS](../vs140/-HEADERS.md) DUMPBIN option is available for use on files produced with the [/GL](../Topic/-GL%20\(Whole%20Program%20Optimization\).md) compiler option.  
  
## See Also  
 [DUMPBIN Options](../vs140/DUMPBIN-Options.md)