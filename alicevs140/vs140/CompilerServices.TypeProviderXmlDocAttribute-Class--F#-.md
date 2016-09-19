---
title: "CompilerServices.TypeProviderXmlDocAttribute Class (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 15df1059-16f1-4855-ab6a-860d60003c90
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CompilerServices.TypeProviderXmlDocAttribute Class (F#)
The `TypeProviderXmlDocAttribute` attribute can be added to types and members. The language service will display the [CommentText](../vs140/TypeProviderXmlDocAttribute.CommentText-Property--F#-.md) property from the attribute in the appropriate place when the user  performs either of the following steps:  
  
-   Points to a type or member in the Visual Studio editor.  
  
-   Moves the cursor so that it appears next to or within the name of a type or member and then chooses the Ctrl+K, I keys.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.CompilerServices  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(32767, AllowMultiple = false)>]  
type TypeProviderXmlDocAttribute =  
 class  
  new TypeProviderXmlDocAttribute : string -> TypeProviderXmlDocAttribute  
  member this.CommentText : string  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `TypeProviderXmlDoc`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/CompilerServices.TypeProviderXmlDocAttribute-Constructor--F#-.md)|Creates an instance of the attribute.|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[CommentText](../vs140/TypeProviderXmlDocAttribute.CommentText-Property--F#-.md)|The text that describes the generated type or member.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core.CompilerServices Namespace (F#)](../vs140/Microsoft.FSharp.Core.CompilerServices-Namespace--F#-.md)