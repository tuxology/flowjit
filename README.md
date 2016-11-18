FlowJIT
=======

The FlowJIT mechanism allows reconstruction of runtime compiled code when hardware tracing is used for program flow tracing. This patch has been tested with Intel PT on a eBPF program compiled in userspace with uBPF and on static key instrumentation scenario. Hardware traces have been successfully reconstructed in our test scenarios.

Usage
-----

Apply the patch on Linux Kernel v4.7 and recompile kernel with the new FlowJIT configuration `CONFIG_TRACING_EXEC_PAGE=y`. After recompilation, `flowjit-agent` is required to run the target process and activate it for tracking.


(C) 2016 Suchakrapani Sharma <suchakrapani.sharma@polymtl.ca>
