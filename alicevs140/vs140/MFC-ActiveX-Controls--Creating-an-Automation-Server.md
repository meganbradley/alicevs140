---
title: "MFC ActiveX Controls: Creating an Automation Server"
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
ms.assetid: e0c24ed2-d61c-49ad-a4fa-4e1098d1d39b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC ActiveX Controls: Creating an Automation Server
You can develop an MFC ActiveX control as an Automation server for the purpose of programmatically embedding that control in another application and calling methods in the control from the application. Such a control would still be available to be hosted in an ActiveX control container.  
  
### To create a control as an Automation server  
  
1.  [Create](../vs140/MFC-ActiveX-Control-Wizard.md) the control.  
  
2.  [Add methods](../vs140/MFC-ActiveX-Controls--Methods.md).  
  
3.  Override [IsInvokeAllowed](../vs140/COleControl--IsInvokeAllowed.md). For more information, see Knowledge Base article Q146120.  
  
4.  Build the control.  
  
### To programmatically access the methods in an Automation server  
  
1.  Create an application, for example, an [MFC exe](../vs140/MFC-Application-Wizard.md).  
  
2.  At the beginning of the `InitInstance` function, add the following line:  
  
     [!CODE [NVC_MFC_AxCont#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxCont#17)]  
  
3.  In Class View, right-click the project node and select **Add class from typelib** to import the type library.  
  
     This will add files with the file name extensions .h and .cpp to the project.  
  
4.  In the header file of the class where you will call one or more methods in the ActiveX control, add the following line: `#include filename.h`, where file name is the name of the header file that was created when you imported the type library.  
  
5.  In the function where a call will be made to a method in the ActiveX control, add code that creates an object of the control's wrapper class and create the ActiveX object. For example, the following MFC code instantiates a `CCirc` control, gets the Caption property, and displays the result when the OK button is clicked in a dialog box:  
  
     [!CODE [NVC_MFC_AxCont#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxCont#18)]  
  
 If you add methods to the ActiveX control after you use it in an application, you can begin using the latest version of the control in the application by deleting the files that were created when you imported the type library. Then import the type library again.  
  
## See Also  
 [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)