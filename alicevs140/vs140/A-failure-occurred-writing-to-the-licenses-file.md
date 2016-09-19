---
title: "A failure occurred writing to the licenses file"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7ea1e2ac-fc94-4d53-8ce9-2ae31bcba85d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A failure occurred writing to the licenses file
The transformed file could not be written to by the project system. As part of preparing licenses, the project system will transform text .licx files into binary licenses files that are understood by the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] licensing system.  
  
 Possible reasons for this error include no disk space left on the device or exceeding the MAX_PATH limit for file names.  
  
 **To correct this error**  
  
-   Move the project to a different folder with a short absolute path name or shorten the output file name.  
  
     The build process will fail if this error occurs.  
  
## See Also  
 [Licensing Components and Controls](assetId:///8e66c1ed-a445-4b26-8185-990b6e2bbd57)