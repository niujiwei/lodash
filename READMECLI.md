Custom Builds
Custom builds make it easy to create lightweight versions of Lodash containing only the features you need. To top it off, we handle all function dependency & alias mapping for you. Review the build differences & pick the one that’s right for you.

The Lodash command-line interface is available when lodash-cli is installed as a global package:

$ npm i -g npm
$ npm i -g lodash-cli
$ lodash -h
Build Types
Core builds, that are 4 kB, are created using the core modifier.
lodash core
Strict builds, with ES strict mode enabled, are created using the strict modifier.
lodash strict
Modularized builds, with Lodash split into modules, are created using the modularize modifier.
lodash modularize
Build Commands:
Use the category command to pass comma separated categories of functions to include in the build.
Valid categories are “array”, “collection”, “date”, “function”, “lang”, “object”, “number”, “seq”, “string”, & “util”.
lodash category=collection,function
Use the exports command to pass comma separated names of ways to export the lodash function.
Valid exports are “amd”, “commonjs”, “es”, “global”, “node”, “npm”, “none”, & “umd”.
lodash exports=amd,node
Use the iife command to specify code to replace the IIFE that wraps Lodash.
lodash iife="\!function(window,undefined){%output%}(this)"
Use the include command to pass comma separated names of functions to include in the build.
lodash include=each,filter,map
Use the minus command to pass comma separated function/category names to remove from the build.
lodash minus=result,shuffle
Use the plus command to pass comma separated function/category names to add to the build.
lodash category=array plus=random,template
Use the template command to pass the file path pattern used to match template files to precompile.
Note: Precompiled templates are assigned to the _.templates object.
lodash template="./*.jst"
Use the settings command to pass template settings used when precompiling templates.
lodash settings="{interpolate:/\{\{([sS]+?)\}\}/g}"
Use the moduleId command to specify the AMD module ID for Lodash or the module ID used to include Lodash in compiled templates.
Use “none” as the module ID to create compiled templates without a dependency on Lodash.
lodash moduleId=underscore
Notes:
The exports values “es” & “npm” may only be used in conjunction with the modularize command
The modularize command uses the first exports values as its module format, ignoring subsequent values
Unless specified by -o or --output all files created are saved to the current working directory
The following options are also supported:

-c, --stdout ................ Write output to standard output
-d, --development ..... Write only the non-minified development output
-h, --help .................... Display help information
-m, --source-map ....... Generate a source map using an optional source map URL
-o, --output ................ Write output to a given path/filename
-p, --production ....... Write only the minified production output
-s, --silent ............... Skip status updates normally logged to the console
-V, --version ............. Output current version of Lodash
