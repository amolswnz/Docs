# Installation
0. npm install express --global
0. npm install express-generator -g
0. Create and Enter in ProjectFoler
0. express -H (Install with Hogen.js Generator)
0. npm install 
0. npm install swig --save (Install swig)
0. Change from hjs to swig
`var swig = require('swig');
    app.engine('html', swig.renderFile);
    app.set('view engine', 'html');`
0. Rename default views files from hjs to html
0. npm uninstall hjs --save
0. npm install mongoose --save
0. npm start or nodemon (Run Application)
0. http://localhost:3000/
0. `var mongoose = require('mongoose');
mongoose.connect('mongodb://127.0.0.1:27017/standup');
mongoose.Promise = global.Promise;
`

