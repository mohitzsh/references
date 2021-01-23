
- While using Gitbook-cli, I was running into issues with XCode not available. The root cause of this issue is incompatibility of https://github.com/nodejs/node-gyp with Catalina 10.15. I am taking these notes to understand the nodejs ecosystem better:
  - node-gyp is native addon build tool. So what exactly are nodejs addons.
  - nodejs addons:
    - Addons are dynamically-linked shared objects written in C++ (source : [nodejs addons](https://nodejs.org/api/addons.html))
  - Installing nodejs (with proper node-gyp installation) on OSX Catalina 10.15
    - [Official node-gyp guide](https://github.com/nodejs/node-gyp/blob/master/macOS_Catalina.md)
    - Installed nodejs from the macOX installed from the official site: https://nodejs.org/en/#home-downloadhead
      - nodejs version: v14.15.4
      - npm version: 6.14.10
 
    - Fixed the commandline tools issue following the steps in [this](https://github.com/nodejs/node-gyp/blob/master/macOS_Catalina.md#installing-node-gyp-using-the-xcode-command-line-tools-via-xcode-select---install) section of the document.
    
    - Had a quick question: Should I install node-gyp using npm before installing gitbook-cli or does node-gyp get installed as a dependency of gitbook-cli?
      - Let's install gitbook-cli and see if that works.
        - npm install gitbook-cli -g gives this error -- npm WARN checkPermissions Missing write access to /usr/local/lib/node_modules
        - Seems like a fairly common issue. Following the highest voted answer on stackoverflow https://stackoverflow.com/questions/33725639/npm-install-g-less-does-not-work-eacces-permission-denied
          - It worked.
        - The same issue with the `gitbook init` call. I guess gitbook-cli package is using its own version of node-gyp which is not installed following the recommended way.
      - Uninstall gitbook-cli and reinstall after installing node-gyp and making sure that gitbook-cli uses your _proper_ node-gyp installation.
      
