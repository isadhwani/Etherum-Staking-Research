##What is Typescript?
Typescript has all functionality of Javascript but allows us to use type interfaces. Typescript supports a tighter integration with editors, making it easier to use. We reccomend using Jetbrains software, Webstorm or VS code as your editor. If you are familiar with Javascript syntax, moving to Typescript should be simple

##Running a Typescript program
Type script can be run from the command line by using two commands: tsc and node. An example of running a Typescript program looks like this

### tsc && node src/path/to/program.js

Note that the program you are actually running is a Javascript file. When you run tsc, it converts all .ts files into corresponding .js files. Where tsc looks for .ts files and where it writes the .js files can be configured in the tsconfig.json file. 
Running the tsc command sometimes takes a long time to compile. While you may not notice this with only a couple .ts files, you will soon be running code with many more files. Instead of running tsc everytime, you can create a new run configuration that only converts newly changed .ts files into .js files. In Webstorm, you can do this by clicking the current file dropdown on the top left of the window. Then go to new configuration > Add new > Node.js. In the next window, under JavaScirpt file click on the browse file option. Navigate to the .js file you would like to run inside the src folder(not ts_src!) You can now run this file by clicking the green play button on the top left. 

##Typescript Congiurations
The tsconfig.json file tells tsc how to run ts programs. You can find an example of a tsconfig file in the bitcoin.js-lib, or use our tsconfig located in utils. 
