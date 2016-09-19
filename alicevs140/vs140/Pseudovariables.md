---
title: "Pseudovariables"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fae84f68-2138-4144-9bd4-c9e271b6182a
caps.latest.revision: 37
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Pseudovariables
Pseudovariables are terms used to display certain information in a variable window or the **QuickWatch** dialog box. You can enter a pseudovariable the same way you would enter a normal variable. Pseudovariables are not variables, however, and do not correspond to variable names in your program.  
  
## Example  
 Suppose you are writing a native code application and want to see the number of handles allocated in your application. In the **Watch** window, you can enter the following pseudovariable in the **Name** column, then press Return to evaluate it:  
  
```  
$handles  
```  
  
 In native code, you can use the pseudovariables shown in this table:  
  
|Pseudovariable|Function|  
|--------------------|--------------|  
|`$err`|Displays the last error value set with the function SetLastError. The value that is displayed represents what would be returned by the GetLastError function.<br /><br /> Use `$err,hr` to see the decoded form of this value. For example, if the last error was 3, the `$err,hr` would display `ERROR_PATH_NOT_FOUND : The system cannot find the path specified.`|  
|`$handles`|Displays the number of handles allocated in your application.|  
|`$vframe`|Displays the address of the current stack frame.|  
|`$tid`|Displays the thread ID for the current thread.|  
|`$env`|Displays the environment block in the string viewer.|  
|`$cmdline`|Displays the command line string that launched the program.|  
|`$pid`|Displays the process id.|  
|`$` *registername*<br /><br /> or<br /><br /> `@` *registername*|Displays the contents of the register *registername*.<br /><br /> Normally, you can display register contents just by entering the register name. The only time you need to use this syntax is when the register name overloads a variable name. If the register name is the same as a variable name in the current scope, the debugger interprets the name as a variable name. That's when `$`*registername* or `@`*registername* comes in handy.|  
|`$clk`|Displays the time in clock cycles.|  
|`$user`|Displays a structure with account information for the account running the application. For security reasons, the password information is not displayed.|  
|`$exceptionstack`|Displays the stack trace of the current Windows Runtime exception. `$ exceptionstack` works only in Store apps that are running on Windows 8.1 or later. `$ exceptionstack` is not supported for C++ and SHE exceptions|  
|`$ReturnValue`|Displays the return value of a .NET Framework method. See [Examine return values of method calls](../vs140/Examine-return-values-of-method-calls.md)|  
  
 In C# and Visual Basic, you can use the pseudovariables shown in this table:  
  
|Pseudovariable|Function|  
|--------------------|--------------|  
|`$exception`|Displays information on the last exception. If no exception has occurred, evaluating `$exception` displays an error message.<br /><br /> In Visual C# only, when the Exception Assistant is disabled, `$exception` is automatically added to the **Locals** window when an exception occurs.|  
|`$user`|Displays a structure with account information for the account running the application. For security reasons, the password information is not displayed.|  
  
 In Visual Basic, you can use the pseudovariables shown in the following table:  
  
|Pseudovariable|Function|  
|--------------------|--------------|  
|`$delete` or `$$delete`|Deletes an implicit variable that was created in the **Immediate** window. The syntax is `$delete,` *variable* or`$delete,` *variable*`.`|  
|`$objectids` or `$listobjectids`|Displays all active Object IDs as children of the specified expression. The syntax is `$objectid,` *expression* or`$listobjectids,` *expression*`.`|  
|`$` *N* `#`|Displays object with Object ID equal to *N*.|  
|`$dynamic`|Displays the special **Dynamic View** node for an object that implements the `IDynamicMetaObjectProvider`. Interface. The syntax is `$dynamic,` *object*. This feature applies only to code that uses .NET Framework version 4. See [Dynamic View](../vs140/Dynamic-View.md).|  
  
## See Also  
 [How to: Watch an Expression in the Debugger](../vs140/Watch-and-QuickWatch-Windows.md)   
 [Debugger Variable Windows](../vs140/Variable-Windows.md)