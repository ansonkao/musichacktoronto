#Kickstarter for Bootstrap themes

##Structure of the assets

The structure of the assets is described in detail over here: <https://team.micromata.de/confluence/display/UXTEAM/Bootstrap+Workflow>

##Setup of external sources

Bootstrap and jQuery are installed via Bower. You can check the availability of bower with typing the following into your terminal:

	bower --version
	
Your Terminal should response with the version number of Bower if Bower is installed properly. Something like:

	1.3.5
	
Otherwise you have to install Bower first.

### Installing Bower
[Bower][bower] depends on Node and npm. 

So you have to install [Node.js][node] first in case you don’t have it installed already.

If your not sure about the availability of these just type the flowing into your terminal to check wether it’s existing or not: 

	npm --version  

Your Terminal should response with the version number of npm if node is installed properly. Something like:

	1.4.10

You can continue with the global installation of bower using npm in that case:

	npm install -g bower	

Also make sure that git is installed as some bower packages require it to be fetched and installed.

[node]: http://nodejs.org/
[bower]: http://bower.io/

### Installing external resources

Just fire the following in the terminal:

	cd path/to/your/checkout/of/kickstarter
	bower install
	
That should place a `lib` directory containing the dependencies defined in the `bower.json` in your root directory of the project.

### Changing version of external resources

You can change the version of the external resources by editing the `bower.json` file within the root directory of the project.

	"dependencies": {
	    "bootstrap": "~3.1",
	    "jquery": "~1.11"
	}
	
The `~` means: Install the latest version including dot-releases.

So `~1.11` installed the latest 1.11.x release which is version 1.11.1 in case of jQuery right now. So if jQuery 1.11.2 will be fetched as soon as it is released when you fire `bower update` or `bower install`. But Bower won’t install jQuery 1.12 or later.

Check <http://semver-ftw.org> for more information about »Semantic Versioning«.