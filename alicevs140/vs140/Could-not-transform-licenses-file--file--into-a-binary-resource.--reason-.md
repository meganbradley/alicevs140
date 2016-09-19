---
title: "Could not transform licenses file &#39;file&#39; into a binary resource. &lt;reason&gt;"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 875e948c-d7a3-4ffc-be0d-f341de5f6310
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Could not transform licenses file &#39;file&#39; into a binary resource. &lt;reason&gt;
The licenses processor used to transform .licx files into binary resources failed for some reason.  
  
 This error is typically caused by a bad .licx file. For example, the file may have been opened and modified in a text editor.  
  
 The build process will fail if this error occurs.  
  
### To correct this error  
  
1.  Select the project in Solution Explorer.  
  
2.  From the **Project** menu, click **Show All Files**.  
  
3.  In the Solution Explorer, expand the obj folder, and then expand the **Debug** folder.  
  
4.  Locate the file named "myApplication.exe.licenses" where myApplication is the name of your Windows Forms application.  
  
5.  Delete this file and rebuild the solution.  
  
## See Also  
 [Licensing Components and Controls](assetId:///8e66c1ed-a445-4b26-8185-990b6e2bbd57)