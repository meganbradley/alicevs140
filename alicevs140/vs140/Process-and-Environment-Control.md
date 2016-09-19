---
title: "Process and Environment Control"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7fde74c3-c2a6-4d15-84b8-092160d60c3e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Process and Environment Control
Use the process-control routines to start, stop, and manage processes from within a program. Use the environment-control routines to get and change information about the operating-system environment.  
  
### Process and Environment Control Functions  
  
|Routine|Use|.NET Framework equivalent|  
|-------------|---------|-------------------------------|  
|[abort](../vs140/abort.md)|Abort process without flushing buffers or calling functions registered by `atexit` and `_onexit`|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[assert](../vs140/assert-Macro--_assert--_wassert.md)|Test for logic error|[System::Diagnostics::Debug::Assert](https://msdn.microsoft.com/en-us/library/system.diagnostics.debug.assert.aspx)|  
|[_ASSERT, _ASSERTE](../vs140/_ASSERT--_ASSERTE--_ASSERT_EXPR-Macros.md) macros|Similar to `assert`, but only available in the debug versions of the run-time libraries|[System::Diagnostics::Debug::Assert](https://msdn.microsoft.com/en-us/library/system.diagnostics.debug.assert.aspx)|  
|[atexit](../vs140/atexit.md)|Schedule routines for execution at program termination|[System::Diagnostics::Process::Exited](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.exited.aspx)|  
|[_beginthread, _beginthreadex](../vs140/_beginthread--_beginthreadex.md)|Create a new thread on a Windows operating system process|[System::Threading::Thread::Start](https://msdn.microsoft.com/en-us/library/system.threading.thread.start.aspx)|  
|[_cexit](../vs140/_cexit--_c_exit.md)|Perform `exit` termination procedures (such as flushing buffers), then return control to calling program without terminating process|[System::Diagnostics::Process::CloseMainWindow](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.closemainwindow.aspx)|  
|[_c_exit](../vs140/_cexit--_c_exit.md)|Perform `_exit` termination procedures, then return control to calling program without terminating process|[System::Diagnostics::Process::CloseMainWindow](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.closemainwindow.aspx)|  
|[_cwait](../vs140/_cwait.md)|Wait until another process terminates|[System::Diagnostics::Process::WaitForExit](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.waitforexit.aspx)|  
|[_endthread, _endthreadex](../vs140/_endthread--_endthreadex.md)|Terminate a Windows operating system thread|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[_execl, _wexecl](../vs140/_execl--_wexecl.md)|Execute new process with argument list|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_execle, _wexecle](../vs140/_execle--_wexecle.md)|Execute new process with argument list and given environment|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_execlp, _wexeclp](../vs140/_execlp--_wexeclp.md)|Execute new process using `PATH` variable and argument list|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_execlpe, _wexeclpe](../vs140/_execlpe--_wexeclpe.md)|Execute new process using `PATH` variable, given environment, and argument list|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_execv, _wexecv](../vs140/_execv--_wexecv.md)|Execute new process with argument array|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_execve, _wexecve](../vs140/_execve--_wexecve.md)|Execute new process with argument array and given environment|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_execvp, _wexecvp](../vs140/_execvp--_wexecvp.md)|Execute new process using `PATH` variable and argument array|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_execvpe, _wexecvpe](../vs140/_execvpe--_wexecvpe.md)|Execute new process using `PATH` variable, given environment, and argument array|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[exit](../vs140/exit--_Exit--_exit.md)|Call functions registered by `atexit` and `_onexit`, flush all buffers, close all open files, and terminate process|[System::Diagnostics::Process::Kill](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.kill.aspx)|  
|[_exit](../vs140/exit--_Exit--_exit.md)|Terminate process immediately without calling `atexit` or `_onexit` or flushing buffers|[System::Diagnostics::Process::Kill](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.kill.aspx)|  
|[getenv, _wgetenv](../vs140/getenv--_wgetenv.md), [getenv_s, _wgetenv_s](../vs140/getenv_s--_wgetenv_s.md)|Get value of environment variable|[System::Environment::GetEnvironmentVariable](https://msdn.microsoft.com/en-us/library/system.environment.getenvironmentvariable.aspx)|  
|[_getpid](../vs140/_getpid.md)|Get process ID number|[System::Diagnostics::Process::Id](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.id.aspx)|  
|[longjmp](../vs140/longjmp.md)|Restore saved stack environment; use it to execute a nonlocal `goto`|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[_onexit](../vs140/_onexit--_onexit_m.md)|Schedule routines for execution at program termination; use for compatibility with Microsoft C/C++ version 7.0 and earlier|[System::Diagnostics::Process::Exited](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.exited.aspx)|  
|[_pclose](../vs140/_pclose.md)|Wait for new command processor and close stream on associated pipe|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[perror, _wperror](../vs140/perror--_wperror.md)|Print error message|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[_pipe](../vs140/_pipe.md)|Create pipe for reading and writing|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[_popen, _wpopen](../vs140/_popen--_wpopen.md)|Create pipe and execute command|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[_putenv, _wputenv](../vs140/_putenv--_wputenv.md), [putenv_s, _wputenv_s](../vs140/_putenv_s--_wputenv_s.md)|Add or change value of environment variable|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[raise](../vs140/raise.md)|Send signal to calling process|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[setjmp](../vs140/setjmp.md)|Save stack environment; use to execute non local `goto`|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[signal](../vs140/signal.md)|Handle interrupt signal|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[_spawnl, _wspawnl](../vs140/_spawnl--_wspawnl.md)|Create and execute new process with specified argument list|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_spawnle, _wspawnle](../vs140/_spawnle--_wspawnle.md)|Create and execute new process with specified argument list and environment|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_spawnlp, _wspawnlp](../vs140/_spawnlp--_wspawnlp.md)|Create and execute new process using `PATH` variable and specified argument list|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_spawnlpe, _wspawnlpe](../vs140/_spawnlpe--_wspawnlpe.md)|Create and execute new process using `PATH` variable, specified environment, and argument list|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_spawnv, _wspawnv](../vs140/_spawnv--_wspawnv.md)|Create and execute new process with specified argument array|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_spawnve, _wspawnve](../vs140/_spawnve--_wspawnve.md)|Create and execute new process with specified environment and argument array|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_spawnvp, _wspawnvp](../vs140/_spawnvp--_wspawnvp.md)|Create and execute new process using `PATH` variable and specified argument array|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[_spawnvpe, _wspawnvpe](../vs140/_spawnvpe--_wspawnvpe.md)|Create and execute new process using `PATH` variable, specified environment, and argument array|[System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx), [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)|  
|[system, _wsystem](../vs140/system--_wsystem.md)|Execute operating-system command|[System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx), [System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx)|  
  
 In the Windows operating system, the spawned process is equivalent to the spawning process. Any process can use `_cwait` to wait for any other process for which the process ID is known.  
  
 The difference between the `_exec` and `_spawn` families is that a `_spawn` function can return control from the new process to the calling process. In a `_spawn` function, both the calling process and the new process are present in memory unless `_P_OVERLAY` is specified. In an `_exec` function, the new process overlays the calling process, so control cannot return to the calling process unless an error occurs in the attempt to start execution of the new process.  
  
 The differences among the functions in the `_exec` family, as well as among those in the `_spawn` family, involve the method of locating the file to be executed as the new process, the form in which arguments are passed to the new process, and the method of setting the environment, as shown in the following table. Use a function that passes an argument list when the number of arguments is constant or is known at compile time. Use a function that passes a pointer to an array containing the arguments when the number of arguments is to be determined at run time. The information in the following table also applies to the wide-character counterparts of the `_spawn` and `_exec` functions.  
  
### _spawn and _exec Function Families  
  
|Functions|Use PATH variable to locate file|Argument-passing convention|Environment settings|  
|---------------|--------------------------------------|----------------------------------|--------------------------|  
|`_execl, _spawnl`|No|List|Inherited from calling process|  
|`_execle, _spawnle`|No|List|Pointer to environment table for new process passed as last argument|  
|`_execlp, _spawnlp`|Yes|List|Inherited from calling process|  
|`_execlpe, _spawnlpe`|Yes|List|Pointer to environment table for new process passed as last argument|  
|`_execv, _spawnv`|No|Array|Inherited from calling process|  
|`_execve, _spawnve`|No|Array|Pointer to environment table for new process passed as last argument|  
|`_execvp, _spawnvp`|Yes|Array|Inherited from calling process|  
|`_execvpe, _spawnvpe`|Yes|Array|Pointer to environment table for new process passed as last argument|  
  
## See Also  
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)