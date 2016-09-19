---
title: "Debugging Your Provider"
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
ms.assetid: 90d4e7db-06ea-4de0-a7f4-4f3751d50d93
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Debugging Your Provider
There are two ways to debug your provider:  
  
-   Because providers are created in process, you can create some consumer code using the OLE DB consumer templates and step into the provider normally.  
  
-   You can use the ITEST utility that comes with Visual C++.  
  
### To use the ITEST utility  
  
1.  Open the provider project.  
  
2.  On the **Projects** menu, click **Settings**.  
  
3.  In the **Property Pages** dialog box, click the **Debug** tab.  
  
4.  In the **Executable for Debug Session** box, select the ITEST application.  
  
5.  Set breakpoints, and then debug as usual.  
  
## See Also  
 [Working with OLE DB Provider Templates](../vs140/Working-with-OLE-DB-Provider-Templates.md)