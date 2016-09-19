---
title: "MFC ActiveX Controls: Accessing Ambient Properties"
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
ms.assetid: fdc9db29-e6b0-45d2-a879-8bd60e2058a7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC ActiveX Controls: Accessing Ambient Properties
This article discusses how an ActiveX control can access the ambient properties of its control container.  
  
 A control can obtain information about its container by accessing the container's ambient properties. These properties expose visual characteristics, such as the container's background color, the current font used by the container, and operational characteristics, such as whether the container is currently in user mode or designer mode. A control can use ambient properties to tailor its appearance and behavior to the particular container in which it is embedded. However, a control should never assume that its container will support any particular ambient property. In fact, some containers may not support any ambient properties at all. In the absence of an ambient property, a control should assume a reasonable default value.  
  
 To access an ambient property, make a call to [COleControl::GetAmbientProperty](../vs140/COleControl--GetAmbientProperty.md). This function expects the dispatch ID for the ambient property as the first parameter (the file OLECTL.H defines dispatch IDs for the standard set of ambient properties).  
  
 The parameters of the `GetAmbientProperty` function are the dispatch ID, a variant tag indicating the expected property type, and a pointer to memory where the value should be returned. The type of data to which this pointer refers will vary depending on the variant tag. The function returns **TRUE** if the container supports the property, otherwise it returns **FALSE**.  
  
 The following code example obtains the value of the ambient property called "UserMode." If the property is not supported by the container, a default value of **TRUE** is assumed:  
  
 [!CODE [NVC_MFC_AxUI#30](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxUI#30)]  
  
 For your convenience, `COleControl` supplies helper functions that access many of the commonly used ambient properties and return appropriate defaults when the properties are not available. These helper functions are as follows:  
  
-   [COleControl::AmbientBackColor](../vs140/COleControl--AmbientBackColor.md)  
  
-   [AmbientDisplayName](../vs140/COleControl--AmbientDisplayName.md)  
  
-   [AmbientFont](../vs140/COleControl--AmbientFont.md)  
  
    > [!NOTE]
    >  Caller must call **Release( )** on the returned font.  
  
-   [AmbientForeColor](../vs140/COleControl--AmbientForeColor.md)  
  
-   [AmbientLocaleID](../vs140/COleControl--AmbientLocaleID.md)  
  
-   [AmbientScaleUnits](../vs140/COleControl--AmbientScaleUnits.md)  
  
-   [AmbientTextAlign](../vs140/COleControl--AmbientTextAlign.md)  
  
-   [AmbientUserMode](../vs140/COleControl--AmbientUserMode.md)  
  
-   [AmbientUIDead](../vs140/COleControl--AmbientUIDead.md)  
  
-   [AmbientShowHatching](../vs140/COleControl--AmbientShowHatching.md)  
  
-   [AmbientShowGrabHandles](../vs140/COleControl--AmbientShowGrabHandles.md)  
  
 If the value of an ambient property changes (through some action of the container), the **OnAmbientPropertyChanged** member function of the control is called. Override this member function to handle such a notification. The parameter for **OnAmbientPropertyChanged** is the dispatch ID of the affected ambient property. The value of this dispatch ID may be **DISPID_UNKNOWN**, which indicates that one or more ambient properties has changed, but information about which properties were affected is unavailable.  
  
## See Also  
 [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)