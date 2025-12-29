# AI Usage

Briefly describe how you used AI (tools, prompts, code snippets, fixes). Be concise and honest (using AI is fine; it's just a tool; we want to know your method). If you did not use AI, state that here.

Küsisin Geminilt projekti esimest korda jooksutades abi. Esialgu andis frontend käivitades veateate, ei tuvastanud ühte vajaminevat moodulit. Gemini abiga tühjendasin Node'i cache'i ja seejärel sain programmi tööle.

Promptid:
    I am building and running api of java backend and node frontend. I get error: [ERROR] TS2307: Cannot find module './weak_ref.d.js' or its corresponding type declarations. [plugin angular-compiler] Why?

    npm install gives:
        npm error code ENOENT
        npm error syscall open
        npm error path /home/sinxtus/Source/Nortal Leap/nortal-leap-2026-test-assignment/package.json
        npm error errno -2
        npm error enoent Could not read package.json: Error: ENOENT: no such file or directory, open '/home/sinxtus/Source/Nortal Leap/nortal-leap-2026-test-assignment/package.json'
        npm error enoent This is related to npm not being able to find a file.
        npm error enoent
        npm error A complete log of this run can be found in: /home/sinxtus/.npm/_logs/2025-12-28T00_21_55_915Z-debug-0.log

Lahendus:
    Clear Your Build Cache (Most Frequent Fix)

    Sometimes the Angular compiler or the build tool (like Vite or Webpack) holds onto a stale state of the dependency tree.

    Delete the .angular folder in your project root.
    Delete the node_modules folder and the package-lock.json file.
    Run npm install (or yarn install) to fresh-install everything.