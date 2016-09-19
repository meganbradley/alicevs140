---
title: "Selecting a Graphic Object into a Device Context"
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
ms.assetid: cf54a330-63ef-421f-83eb-90ec7bd82eef
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Selecting a Graphic Object into a Device Context
This topic applies to using graphic objects in a window's device context. After you [create a drawing object](../vs140/One-Stage-and-Two-Stage-Construction-of-Objects.md), you must select it into the device context in place of the default object stored there:  
  
 [!CODE [NVC_MFCDocViewSDI#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocViewSDI#7)]  
  
## Lifetime of Graphic Objects  
 The graphic object returned by [SelectObject](../vs140/CDC--SelectObject.md) is "temporary." That is, it will be deleted by the [OnIdle](../vs140/CWinApp--OnIdle.md) member function of class `CWinApp` the next time the program gets idle time. As long as you use the object returned by `SelectObject` in a single function without returning control to the main message loop, you will have no problem.  
  
### What do you want to know more about?  
  
-   [Graphic objects](../vs140/Graphic-Objects.md)  
  
-   [One-stage and two-stage construction of graphic objects](../vs140/One-Stage-and-Two-Stage-Construction-of-Objects.md)  
  
-   [Device contexts](../vs140/Device-Contexts.md)  
  
-   [Drawing in a View](../vs140/Drawing-in-a-View.md)  
  
## See Also  
 [Graphic Objects](../vs140/Graphic-Objects.md)