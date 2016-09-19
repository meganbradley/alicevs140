---
title: "CDynamicParameterAccessor Class"
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
ms.assetid: 5f22626e-e80d-491f-8b3b-cedc50331960
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicParameterAccessor Class
Similar to [CDynamicAccessor](../vs140/CDynamicAccessor-Class.md) but obtains parameter information to be set by calling the [ICommandWithParameters](https://msdn.microsoft.com/en-us/library/ms712937.aspx) interface.  
  
## Syntax  
  
```  
class CDynamicParameterAccessor : public CDynamicAccessor  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[CDynamicParameterAccessor](../vs140/CDynamicParameterAccessor--CDynamicParameterAccessor.md)|The constructor.|  
|[GetParam](../vs140/CDynamicParameterAccessor--GetParam.md)|Retrieves the parameter data from the buffer.|  
|[GetParamCount](../vs140/CDynamicParameterAccessor--GetParamCount.md)|Retrieves the number of parameters in the accessor.|  
|[GetParamIO](../vs140/CDynamicParameterAccessor--GetParamIO.md)|Determines whether the specified parameter is an input or output parameter.|  
|[GetParamLength](../vs140/CDynamicParameterAccessor--GetParamLength.md)|Retrieves the length of the specified parameter stored in the buffer.|  
|[GetParamName](../vs140/CDynamicParameterAccessor--GetParamName.md)|Retrieves the name of a specified parameter.|  
|[GetParamStatus](../vs140/CDynamicParameterAccessor--GetParamStatus.md)|Retrieves the status of the specified parameter stored in the buffer.|  
|[GetParamString](../vs140/CDynamicParameterAccessor--GetParamString.md)|Retrieves the string data of the specified parameter stored in the buffer.|  
|[GetParamType](../vs140/CDynamicParameterAccessor--GetParamType.md)|Retrieves the data type of a specified parameter.|  
|[SetParam](../vs140/CDynamicParameterAccessor--SetParam.md)|Sets the buffer using the parameter data.|  
|[SetParamLength](../vs140/CDynamicParameterAccessor--SetParamLength.md)|Sets the length of the specified parameter stored in the buffer.|  
|[SetParamStatus](../vs140/CDynamicParameterAccessor--SetParamStatus.md)|Sets the status of the specified parameter stored in the buffer.|  
|[SetParamString](../vs140/CDynamicParameterAccessor--SetParamString.md)|Sets the string data of the specified parameter stored in the buffer.|  
  
## Remarks  
 The provider must support `ICommandWithParameters` for the consumer to use this class.  
  
 The parameter information is stored in a buffer created and managed by this class. Obtain parameter data from the buffer by using [GetParam](../vs140/CDynamicParameterAccessor--GetParam.md) and [GetParamType](../vs140/CDynamicParameterAccessor--GetParamType.md).  
  
 For an example demonstrating how to use this class to execute a SQL Server stored procedure and get the output parameter values, see Knowledge Base article Q058860, "HOWTO: Execute Stored Procedure using CDynamicParameterAccessor." Knowledge Base articles are available in the MSDN Library Visual Studio documentation or at [http://support.microsoft.com/](http://support.microsoft.com).  
  
## Requirements  
 **Header**: atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)   
 [CAccessor Class](../vs140/CAccessor-Class.md)   
 [CDynamicAccessor Class](../vs140/CDynamicAccessor-Class.md)   
 [CManualAccessor Class](../vs140/CManualAccessor-Class.md)