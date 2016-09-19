---
title: "Databinding with ActiveX Controls in Visual C++"
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
ms.assetid: afe11d2b-eefe-43ce-958d-82d3d4dee158
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Databinding with ActiveX Controls in Visual C++
Databinding is implemented through two types of ActiveX controls: data controls and data-bound controls.  
  
 **Data controls**  
 A data control is responsible for encapsulating a database query and the retrieved rowset. The Microsoft data controls provide a user interface consisting of a series of buttons to iterate through the data. Visual C++ offers two data access technologies for data controls: [ADO and RDO](../vs140/Data-Access--ADO-and-RDO.md).  
  
> [!IMPORTANT]
>  ADO and RDO data controls are an older technology that was released in a earlier version of Visual Studio, and might not be available in the current version. To use the information in this section, you might have to obtain a earlier release to acquire the appropriate control.  
  
 **Data-bound controls**  
 A data-bound control is responsible for presenting the data. Data-bound controls connect to data controls to receive data and present the data through a variety of user interfaces. A Visual C++ application can also bind variables to data values set in the data-bound controls; see [CWnd::BindProperty](../vs140/CWnd--BindProperty.md).  
  
 For more information about databinding, see:  
  
-   [MFC ActiveX Controls: Using Data Binding in an ActiveX Control](../vs140/MFC-ActiveX-Controls--Using-Data-Binding-in-an-ActiveX-Control.md)  
  
-   [Data Access: ADO and RDO](../vs140/Data-Access--ADO-and-RDO.md)  
  
-   [ADO Databinding](../vs140/ADO-Databinding.md)  
  
-   [RDO Databinding](../vs140/RDO-Databinding.md)  
  
-   [Wrapper Classes](../vs140/Wrapper-Classes.md)  
  
-   [Setting Event Handlers on ActiveX Controls](../vs140/Setting-Event-Handlers-on-ActiveX-Controls.md)  
  
-   [Error Trapping](../vs140/Error-Trapping.md)  
  
-   [Limitations of Databinding](../vs140/Limitations-of-Databinding.md)  
  
## See Also  
 [Data-Bound Controls (ADO and RDO)](../vs140/Data-Bound-Controls--ADO-and-RDO-.md)