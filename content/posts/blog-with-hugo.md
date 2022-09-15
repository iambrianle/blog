---
title: "how to create a blog using hugo (2022)"
date: 2022-08-17T14:35:50+08:00
draft: false
description: in this post, i'll go though how to install hugo and deploy your blog!
tags: ["guide", "hugo"]
categories: ["coding"]
showtoc: true
author: "brian le"
---

![hugo logo!](/hugo-logo.png)

# what is hugo?

hugo is a static site generator that enables you to create static files like html, css, and javascript in advance. it is a go-based open-source project that promises remarkable build times that are unmatched.

# what does it do?

it aids in the converting of markdown files—the formats in which you will write your articles or blog posts—to static files that will be served afterwards.

# how is it different?

this is distinct from more conventional approaches like a wordpress site, which requires a dedicated database and a web server to reply to queries, communicate with the database, and serve the files on each request. since nothing is dynamic and we know the material won't change, it is much slower than utilising a static-site generator like hugo. http web servers are very effective and quick in serving only static material. users request files, and the server only needs to provide them. there isn't any additional processing applied.

# the benefits

your website may be set up and hosted anywhere (on gcp cloud storage, aws s3, netlfify, firebase, etc.), and it can be deployed to a cdn (content delivery network) to be cached on a global edge network, which will greatly enhance the performance and speed of page loads. this is crucial for seo and for those with slow internet connections (search engine optimization).

# caveats

that does not, however, imply that hugo cannot be utilised in a dynamic manner. you might not be able to use hugo if your use case is highly complex or involves user input. it could be preferable to use a standard website or single-page application built with react, angular, vue, or svelte. hugo, however, contains all the capabilities you want if all you want is a straightforward blog with a few extras, like the ability for people to leave comments.

# get started

the [hugo documentation](https://gohugo.io/documentation/) is very helpful and elaborate. it is the first place to check in case of references or issues.

## installation

hugo is available in all platforms (windows, macos, and linux), as a binary that you can install, or via a package manager. if you have a compatible package manager, that is the recommended way as it is the easiest and has the least amount of work to maintain

### install using the binaries

availabe from their github [releases](https://github.com/gohugoio/hugo/releases) page. (choose the appropriate platform and type of file). make sure to install it in a location that is somewhere in your `path`. `usr/local/bin` is the best place for linux. otherwise, append the location to your `path` variable.

### install using a package manager

**on windows**

	choco install hugo -confirm

or

	scoop install hugo

---

**on linux and macos** (using homebrew)

	brew install hugo

---

to verify that the installation occurred successfully, run the following command.

	hugo version

there should not be any errors.


## creating the site

change directories into the location you want to create your project. then run the following command with your project's name. this will create folder that contains all the files that you need to get started.

	# creates a new site and project called 'firstblog'
	hugo new site firstblog

change directories into the project directory that was created.

	cd firstblog

you will notice a similar folder structure. the `config.toml` file is where all the variables and settings for your projects live. you will be able to setup and configure most of your website from that one file.

	.
	├── archetypes
	├── config.toml
	├── content
	├── data
	├── layouts
	├── static
	└── themes

if you want to change the file type for your configurations, you can change it to yaml or json depending on your preference. you can copy and paste the contents of the file using a tool like [convertsimple](https://www.convertsimple.com/convert-toml-to-yaml/) to convert the format and syntax.

all of the actual content that you write as markdown files lives inside the `content` directory. you can organize the content in folders, and subfolders, and hugo will automatically take care of organizing the posts as categories or subcategories.

use the following command to create a blank markdown file. you can specify where you want to store this file. if the file name alone is provided, then it is directly placed in the `content` directory.

	hugo create first-post.md

or try the following to place it in `content/posts`:

	hugo create posts/first-post.md

---

### front matter

every markdown file that is created and used for your website has a section on the top that is unique to hugo. it starts and ends with `---`. the syntax used in this is `toml` by default. you can change this default setting with the following command:

	# to convert to yml
	hugo convert toyaml

in the front matter, you can set options for the specific page, meta data, and other configuration that is specific to this particular page. check out the documentation of [front matter](https://gohugo.io/content-management/front-matter/) to learn the different options available.

### install a theme

one of the powers of hugo is to utilize one of the many themes created by the community. check out the [complete list](https://themes.gohugo.io/) and choose one of the themes. install the theme after reading the documentation. this procedure is pretty simple. the majority of the time, you will need to manually or automatically download the code and place it in the `themes` folder before moving it into the folder with the name of the theme you selected.

then make sure to go to the `config` file and update the theme variable with the name of the theme you have chosen.

### running the site

hugo comes with a built-in web server that enables local viewing of the website, continuously checks your files for updates, and restarts itself when necessary.

	hugo server -d

## deployment

hugo creates your website using the following command, outputting the finished static content by default to the `public` directory. if necessary, that can be changed in the `config` file. whatever hosting service you decide to utilise, the contents of this file must be deployed.

	hugo -d

# bonus content

## comments

you can add a comments or discussion section to all of your pages (or select ones) easily using [disqus](https://disqus.com/). instructions and setup is very straightforward and simple.



# stuck?
i suggest watching [this video](https://www.youtube.com/watch?v=hjd9jti_dq4) from envato tuts+ if you're a beginners or alternatively you can read [this article](https://gohugo.io/getting-started/installing) from hugo.

# conclusion
hugo is a perfect blog builder for tech geeks out there. if you're a beginners in coding, i suggest using wordpress to build you're blog. i'll cover wordpress in the future on [my blog](https://notbrian.me/) 
### i'd like to hear from you 
- how did you think of this post?
- do you have any question? 

let me know in the comment!


