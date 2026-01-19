# <img src="offly.png" width="200px" alt="offly">

Free docker hosting and disposable containers in the cloud. Automation, web servers, you name it.

## Features
These are the included features when you sign up to offly. These include your Container Dashboard with a Cloud Terminal, Code Editor, and a File Explorer - Plus our Node.js and REST API for docker containers.

### The offly API
<a href="https://www.npmjs.com/package/node-offly"><img src="https://img.shields.io/npm/v/node-offly.svg"></a>
![NPM Downloads](https://img.shields.io/npm/dm/node-offly)

Our API comes in two forms: The Node.js API, and the REST API. We'll only show you some of our Node.js API here, but everything can be found in our [official documentation](https://offly.pagekite.me/documentation). Note that our APIs also use the same containers from your offly account.

The __offly Node.js API__ is the simplest way to use docker containers in Node.js without any docker installation or payment at all.

To use it, install `node-offly` using NPM:
```bash
npm install node-offly
```

Then import it into your script:
```javascript
const offly = require("node-offly");

offly.init("YOUR_API_KEY"); // Your offly API key
```

> [!NOTE]
> We only require an API key for security, verification, and so you can obviously separate your own docker containers. We will never make you pay or upgrade.

Create a container:
```javascript
offly.createContainer(image, name, password);
```

Start a container:
```javascript
offly.startContainer(name);
```

Execute a shell command inside a container:
```javascript
offly.execCommand(container, command, stream, callback);
```

For example:
```javascript
offly.execCommand("MyContainerName", "ping 8.8.8.8 -c4", true, function(output) {
  if (output.finished) return;
  process.stdout.write(output.stdout);
  process.stderr.write(output.stderr);
});
```

> [!NOTE]
> This is not all you can do with the Node.js API. We only showed you a sneak peak here of what you can really do. See everything in the [official documentation!](https://offly.pagekite.me/documentation)

### Container Dashboard
The Container Dashboard is the place where you can create containers, explore and use files in them, use our cloud VS Code editor, check your container stats and logs, and more.

#### Cloud Terminal
An entire CLI interface to your container right from your browser.
<img alt="Cloud Terminal" src="https://github.com/user-attachments/assets/9f6f1194-7785-4425-ba4a-5a77a7fd5db8" />

#### Cloud Code Editor
A Visual Studio Code editor so you can write code and edit files from your container right in your browser.
<img alt="Cloud Code Editor" src="https://github.com/user-attachments/assets/8ed2d32b-dd95-424c-8675-b7981de791aa" />

#### Cloud File Explorer
An entire place to manage, view, upload, and edit files inside your container right in your browser.
<img width="1919" height="962" alt="cloud-file-explorer" src="https://github.com/user-attachments/assets/562e4bb7-aa24-4d51-81e4-73db5d6eab37" />

Ready to start using our Container Dashboard? If you're already logged in, [visit here](https://offly.pagekite.me/cloud/containers) to go to your Container Dashboard, otherwise [log in](https://offly.pagekite.me/login) or [sign up](https://offly.pagekite.me/signup).

If you're looking for more examples of the dashboard or any other features, you can learn more about them [here](https://offly.pagekite.me/examples).

### The Forum
Our [Forum](https://offly.pagekite.me/forum) is a place for the offly community to connect to discuss feature requests, report bugs, or share their feedback or experiences with offly or any of our services.

It's a great place to get bugs fixed, especially big ones that lots of users are having. However, if you're having a smaller issue that needs to be fixed immediately, you can use our [Instant Bug Fixing](https://offly.pagekite.me/support/bug) page instead.

### Support
We offer 24/7 support, and we promise to respond to emails within 10 hours guaranteed*.

You can contact us at [offly@mail.com](mailto:offly@mail.com) or by using our [contact page](https://offly.pagekite.me/contact). If you have any problems with our GitHub repository or Node.js API/NPM package, you can open an issue in the [Issues tab](https://github.com/Parking-Master/offly/issues).

Note that for __Instant Bug Fixing/Reports__, we don't actually mean instant - really mean that bugs will usually be fixed in less than an hour, and maybe more during special days, or less if a lot of users are reporting the same bug.

## Cookies, Privacy, Terms of Use
To view how we collect, use, and store cookie data on your computer, visit our <a href="https://offly.pagekite.me/cookies">Cookie Policy</a>.

If you're curious or cautious about how we handle your information/data before signing up, we recommend you go over our <a href="https://offly.pagekite.me/privacy">Privacy Policy</a>.

If you want to know commercial uses, freedom of our project, or what happens to users who violate our terms, you should look at our <a href="https://offly.pagekite.me/terms">Terms of Service</a>.

# License
offly and all offly-related services are licensed under the GNU General Public License (GPL) 3.0 License.

[View License](https://offly.pagekite.me/license)

Copyright &copy; 2021-2025 Parking Master

Copyright &copy; 2025 offly
