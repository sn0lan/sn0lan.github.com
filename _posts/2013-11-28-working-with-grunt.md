---
layout: post
date: 2013-10-28 16:50
title: Working with grunt
description: My thoughts on moving from ant to grunt
---

# Working with grunt

Up until 2 weeks ago, grunt.js didnt apeall to me. I always used ant with a build.xml file in order to manage my assets.

I finally bit the bullet recently and made the move to grunt and I dont think I will be looking back anytime soon.

## Advantages

### Syntax and structure

The main advantage, as far as I see it, is the syntax. It's a group of JSON objects, instead of this archaiec build.xml nonsense, so if you are used to working with JS you have already won the battle and wont need to spend much time reading up on how it works.

Take this for example, a basic process to uglify my JS:

	// Minify
		uglify: {
			common: {
				src: [
					"<%= meta.app.site %><%= meta.js.src %>/*.js",
					"!<%= meta.app.site %><%= meta.js.src %>/*.min.js"
				],
				dest: "<%= meta.app.site %><%= meta.js.dest %>/combined.js"
			},
			options: {
				mangle: false
			}
		},

When working with ant, I allways felt my process of changing the build process was:

1. Copy
2. Paste
3. Cross fingers and hope it works.

The syntax for it is terrible! trying to look through different processing is a nightmare!

### Package management with grunt-contrib

Ok, before reading any further, go to [this link](http://) and have a look through the contrib libraries.

Back? Ok, now you have seen the extensive list, you can see that there are tonnes of them. More than likely, the things that you use on a daily basis where in that list (such as sass, js-minify, etc.)

These are all extensions to add into grunt to take away that couple of minutes you spend running a minification script.

Just load it in:

	grunt.loadNpmTasks("grunt-contrib-uglify");
	
Register the task:

	grunt.registerTask("js", ["uglify"]);
	
And write something similar to the code above in syntax and boom! you should now not have to worry about uglifying your js, it runs on the command:

	grunt js

## Conclusion

As I said above, this is only from working with grunt for a couple of weeks, but I am well and truly converted from using ant instead for this.

I will be writing more about this as I get more fimiliar working with it but if you want some more resources, check these out:

- [this link](http://)
- [this link](http://)
- [this link](http://)
- [this link](http://)
- [this link](http://)