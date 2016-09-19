---
title: "&#39;&lt;lsetstmt&gt;&#39; is not declared"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8666dd52-58ea-4b84-b59a-8ebd8b2cb23b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;lsetstmt&gt;&#39; is not declared
'<lsetstmt\>' is not declared. LSet statements are no longer supported; use Microsoft.VisualBasic.LSet instead.  
  
 Several functions that were intrinsic to [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] in previous versions have been moved to the <xref:Microsoft.VisualBasic?qualifyHint=True> namespace. This makes their functionality more generally available to all programming languages.  
  
 **Error ID:** BC30820  
  
### To correct this error  
  
-   Use the `LSet` function in the `Microsoft.VisualBasic` namespace instead.  
  
## See Also  
 [NOT IN BUILD: LSet Function](assetId:///591d286c-6b7a-4350-ae74-99fee00fd964)   
 [Programming Element Support Changes Summary](assetId:///0483590a-6309-449c-a2fa-effa26a03b95)