---
title: "Compiler Options Listed by Category"
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
ms.assetid: c4750dcf-dba0-4229-99b6-45cdecc11729
caps.latest.revision: 66
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Options Listed by Category
This article contains a categorical list of compiler options. For an alphabetical list, see [Compiler Options Listed Alphabetically](../vs140/Compiler-Options-Listed-Alphabetically.md).  
  
### Optimization  
  
|Option|Purpose|  
|------------|-------------|  
|[/O1](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md)|Creates small code.|  
|[/O2](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md)|Creates fast code.|  
|[/Ob](../Topic/-Ob%20\(Inline%20Function%20Expansion\).md)|Controls inline expansion.|  
|[/Od](../Topic/-Od%20\(Disable%20\(Debug\)\).md)|Disables optimization.|  
|[/Og](../vs140/-Og--Global-Optimizations-.md)|Deprecated. Uses global optimizations.|  
|[/Oi](../vs140/-Oi--Generate-Intrinsic-Functions-.md)|Generates intrinsic functions.|  
|[/Os](../vs140/-Os---Ot--Favor-Small-Code--Favor-Fast-Code-.md)|Favors small code.|  
|[/Ot](../vs140/-Os---Ot--Favor-Small-Code--Favor-Fast-Code-.md)|Favors fast code.|  
|[/Ox](../vs140/-Ox--Full-Optimization-.md)|Uses maximum optimization (/Ob2gity /Gs).|  
|[/Oy](../Topic/-Oy%20\(Frame-Pointer%20Omission\).md)|Omits frame pointer. (x86 only)|  
|[/favor](../Topic/-favor%20\(Optimize%20for%20Architecture%20Specifics\).md)|Produces code that is optimized for a specified architecture, or for a range of architectures.|  
  
### Code Generation  
  
|Option|Purpose|  
|------------|-------------|  
|[/arch](../vs140/-arch--x86-.md)|Use SSE or SSE2 instructions in code generation. (x86 only)|  
|[/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md)|Produces an output file to run on the common language runtime.|  
|[/EH](../vs140/-EH--Exception-Handling-Model-.md)|Specifies the model of exception handling.|  
|[/fp](../Topic/-fp%20\(Specify%20Floating-Point%20Behavior\).md)|Specifies floating-point behavior.|  
|[/GA](../vs140/-GA--Optimize-for-Windows-Application-.md)|Optimizes for Windows applications.|  
|[/Gd](../Topic/-Gd,%20-Gr,%20-Gv,%20-Gz%20\(Calling%20Convention\).md)|Uses the `__cdecl` calling convention. (x86 only)|  
|[/Ge](../Topic/-Ge%20\(Enable%20Stack%20Probes\).md)|Deprecated. Activates stack probes.|  
|[/GF](../Topic/-GF%20\(Eliminate%20Duplicate%20Strings\).md)|Enables string pooling.|  
|[/Gh](../Topic/-Gh%20\(Enable%20_penter%20Hook%20Function\).md)|Calls hook function `_penter`.|  
|[/GH](../vs140/-GH--Enable-_pexit-Hook-Function-.md)|Calls hook function `_pexit`.|  
|[/GL](../Topic/-GL%20\(Whole%20Program%20Optimization\).md)|Enables whole program optimization.|  
|[/Gm](../vs140/-Gm--Enable-Minimal-Rebuild-.md)|Enables minimal rebuild.|  
|[/GR](../Topic/-GR%20\(Enable%20Run-Time%20Type%20Information\).md)|Enables run-time type information (RTTI).|  
|[/Gr](../Topic/-Gd,%20-Gr,%20-Gv,%20-Gz%20\(Calling%20Convention\).md)|Uses the `__fastcall` calling convention. (x86 only)|  
|[/GS](../Topic/-GS%20\(Buffer%20Security%20Check\).md)|Checks buffer security.|  
|[/Gs](../vs140/-Gs--Control-Stack-Checking-Calls-.md)|Controls stack probes.|  
|[/GT](../vs140/-GT--Support-Fiber-Safe-Thread-Local-Storage-.md)|Supports fiber safety for data allocated by using static thread-local storage.|  
|[/guard:cf](../vs140/-guard--Enable-Control-Flow-Guard-.md)|Adds control flow guard security checks.|  
|[/Gv](../Topic/-Gd,%20-Gr,%20-Gv,%20-Gz%20\(Calling%20Convention\).md)|Uses the `__vectorcall` calling convention. (x86 and x64 only)|  
|[/Gw](../vs140/-Gw--Optimize-Global-Data-.md)|Enables whole-program global data optimization.|  
|[/GX](../vs140/-GX--Enable-Exception-Handling-.md)|Deprecated. Enables synchronous exception handling. Use [/EH](../vs140/-EH--Exception-Handling-Model-.md) instead.|  
|[/Gy](../vs140/-Gy--Enable-Function-Level-Linking-.md)|Enables function-level linking.|  
|[/GZ](../Topic/-GZ%20\(Enable%20Stack%20Frame%20Run-Time%20Error%20Checking\).md)|Deprecated. Enables fast checks. (Same as [/RTC1](../Topic/-RTC%20\(Run-Time%20Error%20Checks\).md))|  
|[/Gz](../Topic/-Gd,%20-Gr,%20-Gv,%20-Gz%20\(Calling%20Convention\).md)|Uses the `__stdcall` calling convention. (x86 only)|  
|[/homeparams](../Topic/-homeparams%20\(Copy%20Register%20Parameters%20to%20Stack\).md)|Forces parameters passed in registers to be written to their locations on the stack upon function entry. This compiler option is only for the [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)] compilers (native and cross compile).|  
|[/hotpatch](../Topic/-hotpatch%20\(Create%20Hotpatchable%20Image\).md)|Creates a hotpatchable image.|  
|[/Qfast_transcendentals](../vs140/-Qfast_transcendentals--Force-Fast-Transcendentals-.md)|Generates fast transcendentals.|  
|[QIfist](../Topic/-QIfist%20\(Suppress%20_ftol\).md)|Deprecated. Suppresses the call of the helper function `_ftol` when a conversion from a floating-point type to an integral type is required. (x86 only)|  
|[/Qimprecise_fwaits](../vs140/-Qimprecise_fwaits--Remove-fwaits-Inside-Try-Blocks-.md)|Removes `fwait` commands inside `try` blocks.|  
|[/Qpar](../Topic/-Qpar%20\(Auto-Parallelizer\).md)|Enables automatic parallelization of loops.|  
|[/Qpar-report](../vs140/-Qpar-report--Auto-Parallelizer-Reporting-Level-.md)|Enables reporting levels for automatic parallelization.|  
|[/Qsafe_fp_loads](../vs140/-Qsafe_fp_loads.md)|Uses integer move instructions for floating-point values and disables certain floating point load optimizations.|  
|[/Qvec-report (Auto-Vectorizer)](../Topic/-Qvec-report%20\(Auto-Vectorizer%20Reporting%20Level\).md)|Enables reporting levels for automatic vectorization.|  
|[/RTC](../Topic/-RTC%20\(Run-Time%20Error%20Checks\).md)|Enables run-time error checking.|  
|[/volatile](../vs140/-volatile--volatile-Keyword-Interpretation-.md)|Selects how the volatile keyword is interpreted.|  
  
### Output Files  
  
|Option|Purpose|  
|------------|-------------|  
|[/doc](../Topic/-doc%20\(Process%20Documentation%20Comments\)%20\(C-C++\).md)|Processes documentation comments to an XML file.|  
|[/FA](../Topic/-FA,%20-Fa%20\(Listing%20File\).md)|Configures an assembly listing file.|  
|[/Fa](../Topic/-FA,%20-Fa%20\(Listing%20File\).md)|Creates an assembly listing file.|  
|[/Fd](../vs140/-Fd--Program-Database-File-Name-.md)|Renames program database file.|  
|[/Fe](../vs140/-Fe--Name-EXE-File-.md)|Renames the executable file.|  
|[/Fi](../vs140/-Fi--Preprocess-Output-File-Name-.md)|Specifies the preprocessed output file name.|  
|[/Fm](../Topic/-Fm%20\(Name%20Mapfile\).md)|Creates a mapfile.|  
|[/Fo](../Topic/-Fo%20\(Object%20File%20Name\).md)|Creates an object file.|  
|[/Fp](../Topic/-Fp%20\(Name%20.Pch%20File\).md)|Specifies a precompiled header file name.|  
|[/FR](../vs140/-FR---Fr--Create-.Sbr-File-.md) [/Fr](../vs140/-FR---Fr--Create-.Sbr-File-.md)|Generates browser files.|  
  
### Preprocessor  
  
|Option|Purpose|  
|------------|-------------|  
|[/AI](../Topic/-AI%20\(Specify%20Metadata%20Directories\).md)|Specifies a directory to search to resolve file references passed to the [#using](../vs140/#using-Directive--C---.md) directive.|  
|[/C](../vs140/-C--Preserve-Comments-During-Preprocessing-.md)|Preserves comments during preprocessing.|  
|[/D](../Topic/-D%20\(Preprocessor%20Definitions\).md)|Defines constants and macros.|  
|[/E](../vs140/-E--Preprocess-to-stdout-.md)|Copies preprocessor output to standard output.|  
|[/EP](../vs140/-EP--Preprocess-to-stdout-Without-#line-Directives-.md)|Copies preprocessor output to standard output.|  
|[/FI](../Topic/-FI%20\(Name%20Forced%20Include%20File\).md)|Preprocesses the specified include file.|  
|[/FU](../vs140/-FU--Name-Forced-#using-File-.md)|Forces the use of a file name, as if it had been passed to the [#using](../vs140/#using-Directive--C---.md) directive.|  
|[/Fx](../vs140/-Fx--Merge-Injected-Code-.md)|Merges injected code with the source file.|  
|[/I](../vs140/-I--Additional-Include-Directories-.md)|Searches a directory for include files.|  
|[/P](../vs140/-P--Preprocess-to-a-File-.md)|Writes preprocessor output to a file.|  
|[/U](../vs140/-U---u--Undefine-Symbols-.md)|Removes a predefined macro.|  
|[/u](../vs140/-U---u--Undefine-Symbols-.md)|Removes all predefined macros.|  
|[/X](../vs140/-X--Ignore-Standard-Include-Paths-.md)|Ignores the standard include directory.|  
  
### Language  
  
|Option|Purpose|  
|------------|-------------|  
|[/openmp](../Topic/-openmp%20\(Enable%20OpenMP%202.0%20Support\).md)|Enables [#pragma omp](../vs140/omp.md) in source code.|  
|[/vd](../Topic/-vd%20\(Disable%20Construction%20Displacements\).md)|Suppresses or enables hidden `vtordisp` class members.|  
|[/vmb](../vs140/-vmb---vmg--Representation-Method-.md)|Uses best base for pointers to members.|  
|[/vmg](../vs140/-vmb---vmg--Representation-Method-.md)|Uses full generality for pointers to members.|  
|[/vmm](../Topic/-vmm,%20-vms,%20-vmv%20\(General%20Purpose%20Representation\).md)|Declares multiple inheritance.|  
|[/vms](../Topic/-vmm,%20-vms,%20-vmv%20\(General%20Purpose%20Representation\).md)|Declares single inheritance.|  
|[/vmv](../Topic/-vmm,%20-vms,%20-vmv%20\(General%20Purpose%20Representation\).md)|Declares virtual inheritance.|  
|[/Z7](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md)|Generates C 7.0–compatible debugging information.|  
|[/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)|Disables language extensions.|  
|[/Zc](../vs140/-Zc--Conformance-.md)|Specifies standard behavior under [/Ze](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md).|  
|[/Ze](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)|Deprecated. Enables language extensions.|  
|[/ZI](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md)|Includes debug information in a program database compatible with Edit and Continue. (x86 only)|  
|[/Zi](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md)|Generates complete debugging information.|  
|[/Zl](../vs140/-Zl--Omit-Default-Library-Name-.md)|Removes the default library name from the .obj file.|  
|[/Zp](../Topic/-Zp%20\(Struct%20Member%20Alignment\).md) *n*|Packs structure members.|  
|[/Zs](../vs140/-Zs--Syntax-Check-Only-.md)|Checks syntax only.|  
|[/ZW](../vs140/-ZW--Windows-Runtime-Compilation-.md)|Produces an output file to run on the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].|  
  
### Linking  
  
|Option|Purpose|  
|------------|-------------|  
|[/F](../Topic/-F%20\(Set%20Stack%20Size\).md)|Sets stack size.|  
|[/LD](../Topic/-MD,%20-MT,%20-LD%20\(Use%20Run-Time%20Library\).md)|Creates a dynamic-link library.|  
|[/LDd](../Topic/-MD,%20-MT,%20-LD%20\(Use%20Run-Time%20Library\).md)|Creates a debug dynamic-link library.|  
|[/link](../vs140/-link--Pass-Options-to-Linker-.md)|Passes the specified option to LINK.|  
|[/LN](../vs140/-LN--Create-MSIL-Module-.md)|Creates an MSIL module.|  
|[/MD](../Topic/-MD,%20-MT,%20-LD%20\(Use%20Run-Time%20Library\).md)|Compiles to create a multithreaded DLL, by using MSVCRT.lib.|  
|[/MDd](../Topic/-MD,%20-MT,%20-LD%20\(Use%20Run-Time%20Library\).md)|Compiles to create a debug multithreaded DLL, by using MSVCRTD.lib.|  
|[/MT](../Topic/-MD,%20-MT,%20-LD%20\(Use%20Run-Time%20Library\).md)|Compiles to create a multithreaded executable file, by using LIBCMT.lib.|  
|[/MTd](../Topic/-MD,%20-MT,%20-LD%20\(Use%20Run-Time%20Library\).md)|Compiles to create a debug multithreaded executable file, by using LIBCMTD.lib.|  
  
### Precompiled Header  
  
|Option|Purpose|  
|------------|-------------|  
|[/Y-](../vs140/-Y---Ignore-Precompiled-Header-Options-.md)|Ignores all other precompiled-header compiler options in the current build.|  
|[/Yc](../vs140/-Yc--Create-Precompiled-Header-File-.md)|Creates a precompiled header file.|  
|[/Yd](../vs140/-Yd--Place-Debug-Information-in-Object-File-.md)|Places complete debugging information in all object files.|  
|[/Yu](../vs140/-Yu--Use-Precompiled-Header-File-.md)|Uses a precompiled header file during build.|  
  
### Miscellaneous  
  
|Option|Purpose|  
|------------|-------------|  
|[/?](../vs140/-HELP--Compiler-Command-Line-Help-.md)|Lists the compiler options.|  
|[@](../vs140/@--Specify-a-Compiler-Response-File-.md)|Specifies a response file.|  
|[/analyze](../Topic/-analyze%20\(Code%20Analysis\).md)|Enables code analysis.|  
|[/bigobj](../vs140/-bigobj--Increase-Number-of-Sections-in-.Obj-file-.md)|Increases the number of addressable sections in an .obj file.|  
|[/c](../Topic/-c%20\(Compile%20Without%20Linking\).md)|Compiles without linking.|  
|[/cgthreads](../vs140/-cgthreads--Code-Generation-Threads-.md)|Specifies number of cl.exe threads to use for optimization and code generation.|  
|[/errorReport](../vs140/-errorReport--Report-Internal-Compiler-Errors-.md)|Enables you to provide internal compiler error (ICE) information directly to the Visual C++ team.|  
|[/FC](../Topic/-FC%20\(Full%20Path%20of%20Source%20Code%20File%20in%20Diagnostics\).md)|Displays the full path of source code files passed to cl.exe in diagnostic text.|  
|[/FS](../vs140/-FS--Force-Synchronous-PDB-Writes-.md)|Forces writes to the program database (PDB) file to be serialized through MSPDBSRV.EXE.|  
|[/H](../Topic/-H%20\(Restrict%20Length%20of%20External%20Names\).md)|Deprecated. Restricts the length of external (public) names.|  
|[/HELP](../vs140/-HELP--Compiler-Command-Line-Help-.md)|Lists the compiler options.|  
|[/J](../vs140/-J--Default-char-Type-Is-unsigned-.md)|Changes the default `char` type.|  
|[/kernel](../vs140/-kernel--Create-Kernel-Mode-Binary-.md)|The compiler and linker will create a binary that can be executed in the Windows kernel.|  
|[/MP](../vs140/-MP--Build-with-Multiple-Processes-.md)|Builds multiple source files concurrently.|  
|[/nologo](../vs140/-nologo--Suppress-Startup-Banner---C-C---.md)|Suppresses display of sign-on banner.|  
|[/sdl](../vs140/-sdl--Enable-Additional-Security-Checks-.md)|Enables additional security features and warnings.|  
|[/showIncludes](../Topic/-showIncludes%20\(List%20Include%20Files\).md)|Displays a list of all include files during compilation.|  
|[/Tc](../vs140/-Tc---Tp---TC---TP--Specify-Source-File-Type-.md) [/TC](../vs140/-Tc---Tp---TC---TP--Specify-Source-File-Type-.md)|Specifies a C source file.|  
|[/Tp](../vs140/-Tc---Tp---TC---TP--Specify-Source-File-Type-.md) [/TP](../vs140/-Tc---Tp---TC---TP--Specify-Source-File-Type-.md)|Specifies a C++ source file.|  
|[/V](../Topic/-V%20\(Version%20Number\).md)|Deprecated. Sets the version string.|  
|[/w](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md)|Disables all warnings.|  
|[/W0, /W1, /W2, /W3, /W4](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md)|Sets output warning level.|  
|[/w1, /w2, /w3, /w4](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md)|Sets warning level for the specified warning.|  
|[/Wall](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md)|Enables all warnings, including warnings that are disabled by default.|  
|[/wd](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md)|Disables the specified warning.|  
|[/we](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md)|Treats the specified warning as an error.|  
|[/WL](../Topic/-WL%20\(Enable%20One-Line%20Diagnostics\).md)|Enables one-line diagnostics for error and warning messages when compiling C++ source code from the command line.|  
|[/wo](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md)|Displays the specified warning only once.|  
|[/Wp64](../Topic/-Wp64%20\(Detect%2064-Bit%20Portability%20Issues\).md)|Obsolete. Detects 64-bit portability problems.|  
|[/Wv](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md)|Disables warnings introduced by later versions of the compiler.|  
|[/WX](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md)|Treats warnings as errors.|  
|[/Yd](../vs140/-Yd--Place-Debug-Information-in-Object-File-.md)|Deprecated. Places complete debugging information in all object files. Use [/Zi](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md) instead.|  
|[/Yl](../vs140/-Yl--Inject-PCH-Reference-for-Debug-Library-.md)|Injects a PCH reference when creating a debug library.|  
|[/Zm](../Topic/-Zm%20\(Specify%20Precompiled%20Header%20Memory%20Allocation%20Limit\).md)|Specifies the precompiled header memory allocation limit.|  
  
### Deprecated and Removed Compiler Options  
  
|Option|Purpose|  
|------------|-------------|  
|[/clr:noAssembly](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md)|Deprecated. Use [/LN (Create MSIL Module)](../vs140/-LN--Create-MSIL-Module-.md) instead.|  
|[/Fr](../vs140/-FR---Fr--Create-.Sbr-File-.md)|Deprecated. Creates a browse information file without local variables.|  
|[/Ge](../Topic/-Ge%20\(Enable%20Stack%20Probes\).md)|Deprecated. Activates stack probes. On by default.|  
|[/GX](../vs140/-GX--Enable-Exception-Handling-.md)|Deprecated. Enables synchronous exception handling. Use [/EH](../vs140/-EH--Exception-Handling-Model-.md) instead.|  
|[/GZ](../Topic/-GZ%20\(Enable%20Stack%20Frame%20Run-Time%20Error%20Checking\).md)|Deprecated. Enables fast checks. Use [/RTC1](../Topic/-RTC%20\(Run-Time%20Error%20Checks\).md) instead.|  
|[/H](../Topic/-H%20\(Restrict%20Length%20of%20External%20Names\).md)|Deprecated. Restricts the length of external (public) names.|  
|[/Og](../vs140/-Og--Global-Optimizations-.md)|Deprecated. Uses global optimizations.|  
|[QIfist](../Topic/-QIfist%20\(Suppress%20_ftol\).md)|Deprecated. Once used to specify how to convert from a floating-point type to an integral type.|  
|[/V](../Topic/-V%20\(Version%20Number\).md)|Deprecated. Sets the .obj file version string.|  
|[/Yd](../vs140/-Yd--Place-Debug-Information-in-Object-File-.md)|Deprecated. Places complete debugging information in all object files. Use [/Zi](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md) instead.|  
|[/Zc:forScope-](../Topic/-Zc:forScope%20\(Force%20Conformance%20in%20for%20Loop%20Scope\).md)|Deprecated. Disables conformance in for loop scope.|  
|[/Ze](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)|Deprecated. Enables language extensions.|  
|[/Zg](../Topic/-Zg%20\(Generate%20Function%20Prototypes\).md)|Removed in Visual C++ 2015. Generates function prototypes.|  
  
## See Also  
 [C/C++ Building Reference](../vs140/C-C---Building-Reference.md)   
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)