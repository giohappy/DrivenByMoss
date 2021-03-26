# Debug DrivenByMoss extension
- set the env var BITWIG_DEBUG_PORT=5005
- run Bitwig and activate OSC controller
- set breakpoint
- create launch configuration:
    ```
    {
        "type": "java",
        "name": "Debug Bitwig (Attach)",
        "projectName": "DrivenByMoss",
        "request": "attach",
        "hostName": "localhost",
        "port": 5005
    }
    ```
- set a breakpoint in the code
- run `mvn install -Dbitwig.extension.directory=C:\<user>\Documents\Bitwig Studio\Extensions`

Bitwig reloads the extension and will block at he breakpoint
