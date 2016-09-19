---
title: "When Do I Need to Call AtlAxWinInit?"
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
ms.assetid: 080b9cfe-d85a-4439-a9e9-ab3966ebaa8e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# When Do I Need to Call AtlAxWinInit?
[AtlAxWinInit](../vs140/AtlAxWinInit.md) registers the **"AtlAxWin80"** window class (plus a couple of custom window messages) so this function must be called before you try to create a host window. However, you don't always need to call this function explicitly, since the hosting APIs (and the classes that use them) often call this function for you. There is no harm in calling this function more than once. For more information, see [What Is the ATL Control-Hosting API?](../vs140/What-Is-the-ATL-Control-Hosting-API-.md).  
  
## See Also  
 [When Do I Need to Call AtlAxWinTerm?](../vs140/When-Do-I-Need-to-Call-AtlAxWinTerm-.md)   
 [Control Containment FAQ](../vs140/ATL-Control-Containment-FAQ.md)