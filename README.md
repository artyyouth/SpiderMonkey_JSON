Back porting native JSON support from SpiderMonkey 1.85 to SpiderMonkey 1.70.
-----------------------------------------------------------------------------

* What is "native JSON support"?
  - The "JSON" object.
  - "JSON.parse()" function which parse a JS object into JSON string.
  - "JSON.stringify()" function which generate a JS object from a JSON string.

* Why?
  - SpiderMonkey a widely used opensource JS engine. 
  - But the later version since v1.70 requires MinGW to build on Windows platform. 
  - v1.70 is the last version which is able to be compiled into a native Windows lib/dll, but it doesn't have native JSON support.

**This project is to provide a native SpiderMonkey lib/dll on Windows with native JSON support.**

* How to build?
  - Open Visual Studio Command Prompt
  - Debug build: nmake -f "js.mak" CFG="jsshell - Win32 Debug"
  - Release build: nmake -f "js.mak" CFG="jsshell - Win32 Release"
