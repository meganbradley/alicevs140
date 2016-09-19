---
title: "Creating the Provider"
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
ms.assetid: 2506ba8f-010d-4231-aac1-387432f7b6b9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating the Provider
#### To create an OLE DB provider with the ATL OLE DB Provider Wizard  
  
1.  Right-click the project.  
  
2.  On the shortcut menu, click **Add**, and then click **Add Class**.  
  
3.  In the **Add Class** dialog box, select the **ATL OLE DB Provider** icon, and then click **Open**.  
  
4.  In the ATL OLE DB Provider Wizard, enter a short name for your provider in the **Short Name** box. The following topics use the short name "MyProvider", but you can use another name. The other name boxes populate according to the name you enter.  
  
5.  Edit the other name boxes, if needed. In addition to the object and file names, you can edit the following:  
  
    -   **Coclass**: The name that COM uses to create the provider.  
  
    -   **ProgID**: The programmatic identifier, which is a text string that can be used instead of a GUID.  
  
    -   **Version**: Used with the ProgID and coclass to generate a version-dependent programmatic ID.  
  
6.  Click **Finish**.  
  
## See Also  
 [Creating an OLE DB Provider](../vs140/Creating-an-OLE-DB-Provider.md)