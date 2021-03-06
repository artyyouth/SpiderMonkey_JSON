Back porting native JSON support from SpiderMonkey 1.85 to SpiderMonkey 1.70.
-----------------------------------------------------------------------------

* What is "native JSON support"?
  - The "JSON" object.
  - "JSON.parse()" function which parse a JS object into JSON string.
  - "JSON.stringify()" function which generate a JS object from a JSON string.

* Why?
  - SpiderMonkey is a widely used opensource JS engine, I'm also using it to do script binding for some C++ applications. 
  - The JSAPI provide by SpiderMonkey v1.85 has evolved without backward compatibility, a lagcy code base I'm using is not able to upgrade to new API in a short time.
  - SpiderMonkey v1.70 doesn't provide native JSON support, and the later version since v1.70 requires MinGW to build on Windows platform. 

**This project is to provide a native SpiderMonkey lib/dll on Windows with native JSON support.**

* How to build?
  - Open Visual Studio Command Prompt
  - Debug build: nmake -f "js.mak" CFG="jsshell - Win32 Debug"
  - Release build: nmake -f "js.mak" CFG="jsshell - Win32 Release"
