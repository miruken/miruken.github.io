=============
Visual Studio
=============

Debugging with symbols is not enabled by default.  These are the settings that have proven to work with Miruken and SymbolDownloader.

Tools > Options > Debugging > General

    Uncheck "Enable Just My Code"

    Check   "Enable Source Server Support"
    Check   "Print source server diagnostics to the Output window"
    Check   "Allow source server for partial trust assemblies"
    Check   "Always run untrusted source server command without prompting"
    check   "Supress JIT optimization on module load"

Tools > Options > Debugging > Symbols
    
    Set "Cache Symbols in this directory" to c:\temp\symbols    

    Select "Load only specified modules" option

    Click "Specify included modules"

    Add "Miruken.dll" and "Miruken.*.dll" to the list


The "Cache Symbols in this directory" setting must match the "symbolFolder" setting in :code:`Source/config.json`.
You can set it to any folder, but they need to match.
