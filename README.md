# loffice - Lazy Office Analyzer

Requirements:
- Microsoft Office (32-bit)
- WinDbg (x86) - https://msdn.microsoft.com/en-us/windows/hardware/hh852365
- WinAppDbg - http://winappdbg.sourceforge.net/
- Python 2.7 

Loffice is making use of WinAppDbg to extract URLs' from Office documents but also VB-script and Javascipt. By setting strategical breakpoints it's possible to neutralize obfuscation and get the URL and file destination.

Loffice have three different exit-modes which determine if execution is to be aborted:
- url - Exit when the first URL is found
- proc - Exit if a new process is to be created
- none - Do not interupt execution, URL and file information will still be printed.
 
To make analysis as quick as possible macro should be enabled in Office otherwise you would have to manually enable macro for each analysis. After completed analysis the host application (ex. Word) will be terminated.

If you've got any suggestions/thoughts/comments, let me know!

