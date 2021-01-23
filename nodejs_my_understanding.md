
- While using Gitbook-cli, I was running into issues with XCode not available. The root cause of this issue is incompatibility of https://github.com/nodejs/node-gyp with Catalina 15.2. I am taking these notes to understand the nodejs ecosystem better:
  - node-gyp is native addon build tool. So what exactly are nodejs addons.
  - nodejs addons:
    - Addons are dynamically-linked shared objects written in C++ (source : [nodejs addons](https://nodejs.org/api/addons.html))
