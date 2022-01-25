## Getting Started

### Objective

This guide is designed to assist content contributors to start creating content with minimum technical burden. 

### How to add a post

Adding a post can be done as easily as creating a [markdown](https://en.wikipedia.org/wiki/Markdown) file with the naming convention as `file_name.language_code.md`.
*language_code* is a two character code in compliance with [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639-1). Currently the website supports 20 languages including *Arabic, English, French*. 
post must have a [YAML](https://en.wikipedia.org/wiki/YAML) front matter. [Parameters are usually theme specific](https://github.com/Vimux/Mainroad#front-matter-example) but the bare minimum can be as shown in the example below. 

#### Most basic example 

```
#file name : Getting_Started.en.md
---
title: "Getting Started"
date : "2022-01-25"
draft : false 
---     

You write your content here in markdown formats
```

### Adding images

#### Most basic example 

You can add images to your post by simply placing them in side the `/static/images` folder then refernce them using markdown in your post just like in the example below. 

```
# image file exists in /static/img/my_image.png
![exmaple image](/img/my_image.png)
```
If you are HTML savvy, You can customize the size and location of your image within your article.


### Adding new Authors

You can add an authorbox at the end of your post to let the readers know more about you. 
First you need to add your info in the `data/authors` directory. You information should be saved in this manner "yourname.language_code.json" just like in the following example. 

#### Most basic example 
```
#file name : hussain.en.json
{
    "name": "Hussain Alsalman",
    "bio": "Hussain is R lover & developer. He is a data science enthusiast with 10+ years experience in business performance management. He works in IT with Saudi Aramco and holds an MBA in Business Analytics. His blog demonstrates manu use=cases for analytics",
    "avatar": "img/avatar/hussain.png",
    "social": {
        "linkedin": "https://www.linkedin.com/in/hussainalsalman" ,
        "twitter" : "https://www.twitter.com/Arabian_Analyst",
        "website" : "https://www.arabiananalyst.com"
    }
}
```

Please note that you can add your avatar picture in `static/img/avatar/` directory.
Now, all you have to do is to set the author parameter in post YAML fornt matter  as such 

```
----
title: "Getting Started"
date : "2022-01-25"
draft : false 
author : hussain.en
---     
```
**Note**: please make sure that your name matches the file in `data/authors` directory **without** any qoutations.


