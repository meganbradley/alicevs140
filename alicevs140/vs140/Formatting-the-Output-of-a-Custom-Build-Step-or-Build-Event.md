---
title: "Formatting the Output of a Custom Build Step or Build Event"
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
ms.assetid: 92ad3e38-24d7-4b89-90e6-5a16f5f998da
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Formatting the Output of a Custom Build Step or Build Event
If the output of a custom build step or build event is formatted correctly, users get the following benefits:  
  
-   Warnings and errors are counted in the **Output** window.  
  
-   Output appears in the **Task List** window.  
  
-   Clicking on the output in the **Output** window displays the appropriate topic.  
  
-   F1 operations are enabled in the **Task List** window or **Output** window.  
  
 The format of the output should be:  
  
 {*filename* (*line#* [, *column#*]) &#124; *toolname*} **:**  
  
 [*any text*] {**error** &#124; **warning**} *code####***:***localizable string*  
  
 [ *any text* ]  
  
 Where:  
  
-   {*a* &#124; *b*} is a choice of either *a* or *b*.  
  
-   [`ccc`] is an optional string or parameter.  
  
 For example:  
  
 C:\\*sourcefile.cpp*(134) : error C2143: syntax error : missing ';' before '}'  
  
 LINK : fatal error LNK1104: cannot open file '*somelib.lib*'  
  
## See Also  
 [Understanding Custom Build Steps and Build Events](../vs140/Understanding-Custom-Build-Steps-and-Build-Events.md)