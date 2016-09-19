---
title: "Model for Hosting RDO Data Controls in a Container"
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
ms.assetid: ca598bac-9fef-40e6-b6cd-03d817e16b2e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Model for Hosting RDO Data Controls in a Container
A container hosts an RDO data control as follows:  
  
-   The container obtains an IVBDSC interface from the data control. If it cannot find IVBDSC, it is not a data control.  
  
-   The container obtains the **ICursor** interfaces from the data control. These interfaces supply a Cursor object that can be manipulated by a client.  
  
-   The container hooks up to the data control's **INotifyDBEvents** interface. This interface allows the container to receive notifications from the data control. The container should support the **INotifyDBEventsSink** interface to do this.  
  
 A container hosts an RDO data-bound control as follows:  
  
-   The control supports the **IBoundObject** interface and the container supports the **IBoundObjectSite** interface. The control obtains the container's **IBoundObjectSite** interface, and the container obtains the **IBoundObject** interface from the control.  
  
-   The control supports the **IPropNotifySink** interface and hooks up with the container. This allows the container to receive notifications from the control.  
  
-   If the control supports **INotifyDBEventsSink**, it can receive notifications from an RDO data control after connecting with the data control's **INotifyDBEvents** interface.  
  
-   The control then can receive cursor objects from the data control (directly or through the container). The cursors can then be manipulated and scrolled. At this point, the RDO data-bound control is successfully bound.  
  
## See Also  
 [RDO Databinding](../vs140/RDO-Databinding.md)   
 [Using RDO Databinding in Visual C++](../vs140/Using-RDO-Databinding-in-Visual-C--.md)