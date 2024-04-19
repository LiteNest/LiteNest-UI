## LiteNest UI

LiteNest UI is a front-end implementation of the LiteNest container 
cloud desktop platform.

### Features
- **Modern user interface based on Vue 3 and PrimeVue**: Vue 3 is a modern front-end framework that provides a smooth and fast 
user experience through its responsive and efficient design. Combined with PrimeVue's rich component library, the front-end 
design can present a modern and beautiful user interface for users to enhance their visual enjoyment and operating experience.
- **Customizable user interface**: Vue 3 and PrimeVue provide a wealth of components and features that make front-end design 
highly flexible and customizable. Users can customize and extend the front-end interface according to their own needs 
to meet the needs and preferences of different user groups.
- **Responsive layout and components of the user interface**: The front-end design adopts responsive layout and components, 
mainly for the development of computer interfaces. This feature ensures a consistent and good experience for users on 
the desktop side of the browser. The components and layout of the front end design are adjusted according to different 
screen sizes and resolutions to accommodate different sizes and types of displays, improving the convenience and comfort 
of users to access and operate applications on their computers.

### Install
Currently, it can only be installed by compiling the source code. Go to the Release page to download the source code 
package for the release, or get the source code from the clone repository.

1. Before installation, you need to configure the back-end address, the configuration file is located in the project 
directory `public/config.js`, the content of the file is roughly as follows:
```javascript
export const application = {
    baseURL: "http://123.45.78.9:8080",
    remoteBaseURL: "https://123.45.78.9"
}
export const defaultTheme = 'aura-light-blue'
```
There are two properties in the object `application`:
- `baseURL` indicates the http address of the back-end. Do not add `/` at the end.
- `remoteBaseURL` Indicates the address of the remote VNC server. Do not add `/` at the end.

*The system completes VNC connection of remote desktop based on KasmVNC*

2. Execute the command to install packages and build the application.
Make sure Node.js and npm were installed properly on server. Then, execute the following command:
```shell
npm install && npm run build 
```
After a few moments, you can complete the packaging operation.
3. Save the package file:
Copy and save the contents of the `./dist/` folder to a different path (the following example uses `/path/to/frontend` instead)
```shell
cp ./dist/* /path/to/frontend
```

### Run the application
Use any Web server to run the static page you just packaged to complete the front-end work.

**Note that the Web server must have rewriting enabled to ensure that `Vue router` works as expected**