**Tips for building Libjingle on Mac 10.7**

# Introduction #

There are few issues when building Libjingle on a stock Mac 10.7. Before we make official fixes to the code, the following additional steps will walk you through a successful build.


# Details #

After you are done with all steps listed in the README file, please following the following additional steps:
  * Install XCode from the AppStore (version 4.2.1 in my case)
  * Modify the main.scons file with the following two changes:
  * 1. Change the value of '-isysroot' to '/Developer/SDKs/MacOSX10.7.sdk' for both CC and LINK flags
> 2. Remove the line of '-fno-rtti' from the CXXFLAGS section.