---
title: "&#39;&lt;rsetstmt&gt;&#39; is not declared"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7936e3ef-7ac6-4a71-af55-acc2c5cd8754
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;rsetstmt&gt;&#39; is not declared
'<rsetstmt\>' is not declared. RSet statements are no longer supported; use Microsoft.VisualBasic.RSet instead.  
  
 Several functions that were intrinsic to [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] in previous versions have been moved to the <xref:Microsoft.VisualBasic?qualifyHint=True> namespace. This makes their functionality more generally available to all programming languages.  
  
 **Error ID:** BC30821  
  
### To correct this error  
  
-   Use the `RSet` function in the `Microsoft.VisualBasic` namespace instead.  
  
## See Also  
 [NOT IN BUILD: RSet Function](assetId:///534514e5-dee9-4dfd-993b-da09731eece5)   
 [Programming Element Support Changes Summary](assetId:///0483590a-6309-449c-a2fa-effa26a03b95)