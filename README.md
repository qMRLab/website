# qMRLab website

This is the repository that holds the content for the qMRLab website (http://www.qmrlab.org/). Using GitHub pages, commits to this repository will automatically rebuild the final statically generated html pages. If you're interested in more information, check out the guide [here](https://pages.github.com/).

## For content contributors


### Adding author information: _config.yml

Please add an entry in this file (under the 'authors' list) to link between your name and github account (along with other metadata). Sample entry

```
nickname:
  name: Jon Doe
  display_name: Jonny Doe
  email: jonny@gmail.com
  git_name: jodoe
  web: http://jondoe.com
  twitter: https://twitter.com/jodoe
  description: `Interested in qMRI. He is a coffee master ....`
```
* `name`: Self-explanatory
* `nickname`: The name that will appear underneath your image in a blog post. For layout reasons, try to keep this to a single name.
* `github`: Your github handle. *You will need set this in order to post a blog entry*
* `twitter`: (Optional) Your twitter handle. This meta data will appear underneath your image in a blog post.
* `website`: (Optional) A link to your academic website (or other). This meta data will appear underneath your image in a blog post.

### Frontpage: _includes/qmrlab-top.html

The carousel that appears on the top of the page.

If you want to add a new image to the carousel upload the image under assets/images and also add an entry to the file _data/carousel.json. The entry should contain the following meta information:

* `image`: the name of the image as stored under /assets/images/
* `label`: the label that is shown under the image in the carousel
* `color`: the color of the label



### Frontpage: _includes/qmrlab-about.html

An about section that appears just below the carousel banner.


### Frontpage: _includes/contributors.json

An contributors section that appears below the Featured posts section.

The section is generated by taking the metadata about the contributors form the _data/contributors.json.
A single entry in the contributors.json looks like following:

`name`: Full name of the contributor.
`twitter` (Optional): A link to contributor's twitter account
`github`: A link to contributor's github account. This link is also used the get the contributor's github profile picture and display it.
`facebook` (Optional): A link to contributor's facebook account.

If the contributor does not have twitter of facebook account than please set the value for that feature to `#`.

### Frontpage: _includes/affiliation.html

An contributors section that appears at the end of the Frontpage.

The section is generated by fetching the metadata form the _data/affiliations.json.

A single entry in the affiliations.json looks like following:

`name`: The name of the institution.
`image` : The name of the affiliation's image file as stored under /assets/images
`web`: A link to the affiliation's website


## Writing new posts

All blog posts are stored in `_posts` and can be written using markdown using the.
The name of the post file should follow this format YYYY-MM-DD-the-name-of-the-file.md where YYYY-MM-DD is the date when the post was written (Ex. 2018-10-02-hello-world.md ).

At the very top of the post you need to add the following code snippet:



```
---
layout: post
title:  "The title of the post"
author: Author's_Nickname
categories: [ jekyll ]
image: assets/images/image_name.png
featured: false
hidden: false
---

```

*NOTE: The layout and the category tag should not be changed.

* `title` corresponds to the title of the post.
* `author`  corresponds to the nickname of the author  of the post (see the section "Adding author information").
* `image` refer to post's featured image and the value that it takes is the path to the image.  
* The meta tags `featured` and `hidden` are boolean tags that tells whether the post is featured or not and whether the post should be hidden or not, respectively.

After the including all meta information you can start writing your post.
* NOTE: The post should be written in markdown language.
Once you are done with writing please save the post in the folder '_posts' and follow the naming convention described above.


## Problems / Suggestions ?

If you encounter any issues with the site or want to suggest any new website features please create a new GitHub issue.
