---
title: "How to Create a Blog Using Hugo (2022)"
date: 2022-08-17T14:35:50+08:00
draft: false
description: In this post, I'll go through how to install Hugo and deploy your blog!
tags: ["guide", "hugo"]
categories: ["coding"]
showtoc: true
author: "Brian Le"
---

![Hugo Logo](/hugo-logo.png)

# What's Hugo?

Hugo is a static site generator that enables you to create static files like HTML, CSS, and JavaScript in advance. It is a Go-based open-source project that promises remarkable build times that are unmatched.

# What Does It Do?

It aids in the conversion of Markdown files—the formats in which you will write your articles or blog posts—into static files that will be served afterwards.

# How Is It Different?

This is distinct from more conventional approaches like a WordPress site, which requires a dedicated database and a web server to reply to queries, communicate with the database, and serve the files on each request. Since nothing is dynamic and we know the material won't change, it is much slower than utilizing a static-site generator like Hugo. HTTP web servers are very effective and quick in serving only static material. Users request files, and the server only needs to provide them. There isn't any additional processing applied.

# The Benefits

Your website may be set up and hosted anywhere (on GCP Cloud Storage, AWS S3, PaperMod, Firebase, etc.), and it can be deployed to a CDN (Content Delivery Network) to be cached on a global edge network, which will greatly enhance the performance and speed of page loads. This is crucial for SEO and for those with slow internet connections (Search Engine Optimization).

# Caveats

That does not, however, imply that Hugo cannot be utilized in a dynamic manner. You might not be able to use Hugo if your use case is highly complex or involves user input. It could be preferable to use a standard website or single-page application built with React, Angular, Vue, or Svelte. Hugo, however, contains all the capabilities you want if all you want is a straightforward blog with a few extras, like the ability for people to leave comments.

# Get Started

The [Hugo documentation](https://gohugo.io/documentation/) is very helpful and elaborate. It is the first place to check in case of references or issues.

## Installation

Hugo is available on all platforms (Windows, macOS, and Linux), as a binary that you can install, or via a package manager. If you have a compatible package manager, that is the recommended way as it is the easiest and has the least amount of work to maintain.

### Install Using the Binaries

Availabe from their GitHub [releases](https://github.com/gohugoio/hugo/releases) page. (Choose the appropriate platform and type of file). Make sure to install it in a location that is somewhere in your `PATH`. `usr/local/bin` is the best place for Linux. Otherwise, append the location to your `PATH` variable.

### Install Using a Package Manager

**On Windows**

```
choco install hugo -confirm
```

or

```
scoop install hugo
```

---

**On Linux and macOS** (Using Homebrew)

```
brew install hugo
```

---

To verify that the installation occurred successfully, run the following command.

```
hugo version
```

There should not be any errors.

## Creating the Site

Change directories into the location you want to create your project. Then run the following command with your project's name. This will create a folder that contains all the files that you need to get started.

```
# Creates a new site and project called 'firstblog'
hugo new site firstblog
```

Change directories into the project directory that was created.

```
cd firstblog
```

You will notice a similar folder structure. The `config.toml` file is where all the variables and settings for your projects live. You will be able to setup and configure most of your website from that one file.

```
.
├── archetypes
├── config.toml
├── content
├── data
├── layouts
├── static
└── themes
```

If you want to change the file type for your configurations, you can change it to YAML or JSON depending on your preference. You can copy and paste the contents of the file using a tool like [ConvertSimple](https://www.convertsimple.com/convert-toml-to-yaml/) to convert the format and syntax.

All of the actual content that you write as Markdown files lives inside the `content` directory. You can organize the content in folders and subfolders, and Hugo will automatically take care of organizing the posts as categories or subcategories.

Use the following command to create a blank Markdown file. You can specify where you want to store this file. If only the file name is provided, then it is directly placed in the `content` directory.

```
hugo create first-post.md
```

Or try the following to place it in `content/posts`:

```
hugo create posts/first-post.md
```

---

### Front Matter

Every Markdown file that is created and used for your website has a section on the top that is unique to Hugo. It starts and ends with `---`. The syntax used in this is TOML by default. You can change this default setting with the following command:

```
# To convert to YAML
hugo convert toyaml
```

In the front matter, you can set options for the specific page, meta data, and other configuration that is specific to this particular page. Check out the documentation of [Front Matter](https://gohugo.io/content-management/front-matter/) to learn about the different options available.

### Install a Theme

One of the powers of Hugo is the ability to utilize one of the many themes created by the community. Check out the [complete list](https://themes.gohugo.io/) and choose one of the themes. Install the theme after reading the documentation. This procedure is pretty simple. Most of the time, you will need to manually or automatically download the code and place it in the `themes` folder before moving it into the folder with the name of the theme you selected.

Then make sure to go to the `config` file and update the theme variable with the name of the theme you have chosen.

### Running the Site

Hugo comes with a built-in web server that enables local viewing of the website, continuously checks your files for updates, and restarts itself when necessary.

```
hugo server -d
```

## Deployment

Hugo creates your website using the following command, outputting the finished static content by default to the `public` directory. If necessary, that can be changed in the `config` file. Whatever hosting service you decide to utilize, the contents of this file must be deployed.

```
hugo -d
```

# Bonus Content

## Comments

You can add a comments or discussion section to all of your pages (or select ones) easily using [Disqus](https://disqus.com/). Instructions and setup are very straightforward and simple.

# Stuck?

I suggest watching [this video](https://www.youtube.com/watch?v=hjd9jti_dq4) from Envato Tuts+ if you're a beginner or alternatively you can read [this article](https://gohugo.io/getting-started/installing) from Hugo.

# Conclusion

Hugo is a perfect blog builder for tech geeks out there. If you're a beginner in coding, I suggest using WordPress to build your blog. I'll cover WordPress in the future on [my blog](https://notbrian.me/).