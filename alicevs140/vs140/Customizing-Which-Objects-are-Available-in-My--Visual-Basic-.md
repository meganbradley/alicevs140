---
title: "Customizing Which Objects are Available in My (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4e8279c2-ed5b-4681-8903-8a6671874000
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Customizing Which Objects are Available in My (Visual Basic)
This topic describes how you can control which `My` objects are enabled by setting your project's `_MYTYPE` conditional-compilation constant. The [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Integrated Development Environment (IDE) keeps the `_MYTYPE` conditional-compilation constant for a project in sync with the project's type.  
  
## Predefined _MYTYPE Values  
 You must use the `/define` compiler option to set the `_MYTYPE` conditional-compilation constant. When specifying your own value for the `_MYTYPE` constant, you must enclose the string value in backslash/quotation mark (\\") sequences. For example, you could use:  
  
```  
/define:_MYTYPE=\"WindowsForms\"  
```  
  
 This table shows what the `_MYTYPE` conditional-compilation constant is set to for several project types.  
  
|Project type|_MYTYPE value|  
|------------------|--------------------|  
|Class Library|"Windows"|  
|Console Application|"Console"|  
|Web|"Web"|  
|Web Control Library|"WebControl"|  
|Windows Application|"WindowsForms"|  
|Windows Application, when starting with custom `Sub Main`|"WindowsFormsWithCustomSubMain"|  
|Windows Control Library|"Windows"|  
|Windows Service|"Console"|  
|Empty|"Empty"|  
  
> [!NOTE]
>  All conditional-compilation string comparisons are case-sensitive, regardless of how the `Option Compare` statement is set.  
  
## Dependent _MY Compilation Constants  
 The `_MYTYPE` conditional-compilation constant, in turn, controls the values of several other `_MY` compilation constants:  
  
|_MYTYPE|_MYAPPLICATIONTYPE|_MYCOMPUTERTYPE|_MYFORMS|_MYUSERTYPE|_MYWEBSERVICES|  
|--------------|-------------------------|----------------------|---------------|------------------|---------------------|  
|"Console"|"Console"|"Windows"|Undefined|"Windows"|TRUE|  
|"Custom"|Undefined|Undefined|Undefined|Undefined|Undefined|  
|"Empty"|Undefined|Undefined|Undefined|Undefined|Undefined|  
|"Web"|Undefined|"Web"|FALSE|"Web"|FALSE|  
|"WebControl"|Undefined|"Web"|FALSE|"Web"|TRUE|  
|"Windows" or ""|"Windows"|"Windows"|Undefined|"Windows"|TRUE|  
|"WindowsForms"|"WindowsForms"|"Windows"|TRUE|"Windows"|TRUE|  
|"WindowsFormsWithCustomSubMain"|"Console"|"Windows"|TRUE|"Windows"|TRUE|  
  
 By default, undefined conditional-compilation constants resolve to `FALSE`. You can specify values for the undefined constants when compiling your project to override the default behavior.  
  
> [!NOTE]
>  When `_MYTYPE` is set to "Custom", the project contains the `My` namespace, but it contains no objects. However, setting `_MYTYPE` to "Empty" prevents the compiler from adding the `My` namespace and its objects.  
  
 This table describes the effects of the predefined values of the `_MY` compilation constants.  
  
|Constant|Meaning|  
|--------------|-------------|  
|`_MYAPPLICATIONTYPE`|Enables `My.Application`, if the constant is "Console," Windows," or "WindowsForms":<br /><br /> -   The "Console" version derives from <xref:Microsoft.VisualBasic.ApplicationServices.ConsoleApplicationBase?qualifyHint=False>. and has fewer members than the "Windows" version.<br />-   The "Windows" version derives from <xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase?qualifyHint=False>.and has fewer members than the "WindowsForms" version.<br />-   The "WindowsForms" version of `My.Application` derives from <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase?qualifyHint=False>. If the `TARGET` constant is defined to be "winexe", then the class includes a `Sub Main` method.|  
|`_MYCOMPUTERTYPE`|Enables `My.Computer`, if the constant is "Web" or "Windows":<br /><br /> -   The "Web" version derives from <xref:Microsoft.VisualBasic.Devices.ServerComputer?qualifyHint=False>, and has fewer members than the "Windows" version.<br />-   The "Windows" version of `My.Computer` derives from <xref:Microsoft.VisualBasic.Devices.Computer?qualifyHint=False>.|  
|`_MYFORMS`|Enables `My.Forms`, if the constant is `TRUE`.|  
|`_MYUSERTYPE`|Enables `My.User`, if the constant is "Web" or "Windows":<br /><br /> -   The "Web" version of `My.User` is associated with the user identity of the current HTTP request.<br />-   The "Windows" version of `My.User` is associated with the thread's current principal.|  
|`_MYWEBSERVICES`|Enables `My.WebServices`, if the constant is `TRUE`.|  
|`_MYTYPE`|Enables `My.Log`, `My.Request`, and `My.Response`, if the constant is "Web".|  
  
## See Also  
 <xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Devices.Computer?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Logging.Log?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.ApplicationServices.User?qualifyHint=False>   
 [How My Depends on Project Type](../Topic/How%20My%20Depends%20on%20Project%20Type%20\(Visual%20Basic\).md)   
 [Conditional Compilation Overview](../vs140/Conditional-Compilation-in-Visual-Basic.md)   
 [/define (Visual Basic)](../vs140/-define--Visual-Basic-.md)   
 [My.Forms Object](../Topic/My.Forms%20Object.md)   
 [My.Request Object](../vs140/My.Request-Object.md)   
 [My.Response Object](../Topic/My.Response%20Object.md)   
 [My.WebServices Object](../Topic/My.WebServices%20Object.md)