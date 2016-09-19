---
title: "CMyProviderCommand (MyProviderRS.H)"
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
ms.assetid: b30b956e-cc91-4cf5-9fe6-f8b1ce9cc2a5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMyProviderCommand (MyProviderRS.H)
The `CMyProviderCommand` class is the implementation for the provider command object. It provides the implementation for the `IAccessor`, `ICommandText`, and **ICommandProperties** interfaces. The `IAccessor` interface is the same as the one in the rowset. The command object uses the accessor to specify bindings for parameters. The rowset object uses them to specify bindings for output columns. The `ICommandText` interface is a useful way to specify a command textually. This example uses the `ICommandText` interface later when it adds custom code; it also overrides the `ICommand::Execute` method. The **ICommandProperties** interface handles all of the properties for the command and rowset objects.  
  
```  
// CMyProviderCommand  
class ATL_NO_VTABLE CMyProviderCommand :   
class ATL_NO_VTABLE CMyProviderCommand :   
   public CComObjectRootEx<CComSingleThreadModel>,  
   public IAccessorImpl<CMyProviderCommand>,  
   public ICommandTextImpl<CMyProviderCommand>,  
   public ICommandPropertiesImpl<CMyProviderCommand>,  
   public IObjectWithSiteImpl<CMyProviderCommand>,  
   public IConvertTypeImpl<CMyProviderCommand>,  
   public IColumnsInfoImpl<CMyProviderCommand>  
```  
  
 The `IAccessor` interface manages all the bindings used in commands and rowsets. The consumer calls **IAccessor::CreateAccessor** with an array of **DBBINDING** structures. Each **DBBINDING** structure contains the information about how the column bindings should be handled (such as type and length). The provider receives the structures and then determines how the data should be transferred and whether any conversions are necessary. The `IAccessor` interface is used in the command object to handle any parameters in the command.  
  
 The command object also provides an implementation of `IColumnsInfo`. OLE DB requires the `IColumnsInfo` interface. The interface allows the consumer to retrieve information about parameters from the command. The rowset object uses the `IColumnsInfo` interface to return information about the output columns to the provider.  
  
 The provider also contains an interface called `IObjectWithSite`. The `IObjectWithSite` interface was implemented in ATL 2.0 and allows the implementer to pass information about itself to its child. The command object uses the `IObjectWithSite` information to tell any generated rowset objects about who created them.  
  
## See Also  
 [Provider Wizard-Generated Files](../vs140/Provider-Wizard-Generated-Files.md)