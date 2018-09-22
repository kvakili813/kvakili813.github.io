---
layout: post
title:      "Extra! Extra!"
date:       2018-09-22 00:49:18 +0000
permalink:  extra_extra
---


For my first Learn project I was tasked with building a Ruby CLI gem from scratch. My first thought was to keep it simple and design something that I would find useful myself. As a news junkie, I naturally gravitated toward building a headline news reader by scraping content from CNN. 

Initially, I feared looking at a blank canvas, but those fears were quelled when I began following the video guide made by Avi Flombaum and ran the first command in the terminal: 

```
bundle gem  <gem name>
```

By installing the Bundler, the tedious part of my CLI structure was complete and I could now just jump into the code. I realized the most important thing is to just get started with the code and then you begin to get a flow.

The next step was to create the executable file, which would be responsible for providing the interface that the user would interact with. But in order to enable your program to run, the bin file must includ the following code:

```
#!/usr/bin/env ruby
```

### The Structure

Setting up the environment determines not only what kind of libraries are called, but in what order the libraries are called as well. So, it is crucial that the order of execution is done properly, or else your gem will break.

Environment file:

```
require "open-uri"
require "nokogiri"
require "pry"

require_relative "cnn_headlines/version"
require_relative "cnn_headlines/cli.rb"
require_relative "cnn_headlines/topics.rb"
require_relative "cnn_headlines/headlines.rb"
```

### Scraping

For me, the most enojoyable part of this project was scraping. By utilizing Nokogiri, I was able to get exposed to pre-written code and immensely improve my navigation techniques when inspecting the appropriate CSS selectors. Additionally, I gained a better understanding for certain functions like `.gsub` and `.strip` by focusing calling them in action when needed.

### The New Reader

Finally, after creating the classes and objects, I learned how to simplify things. Instead of writing instance methods, I decided to write class methods, which effectively made each method an object of that particular class rather than an isolated instance of the class. The main difference was I no longer needed to establish an initialize method that is required when writing instance methods. By exploring ways to simplify, I also deepened my knowledge of how object orientation works.
