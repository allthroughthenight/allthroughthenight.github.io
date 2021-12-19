# allthroughthenight.github.io

A basic blog for my basic post, all views are my own.

## TODOs

* All-in-one VM set-up via Ansible and Vagrant
* Better understanding of overall static site generators and less-copy-pasta of commands (ಠ_ಠ)

## Topics

* openwrt: blog post pushing packet pushers
* https://www.gfisk.com/disk-clone-windows-activation-0xc004c008/
  * seems like mscft knows when windows is installed on more than one disc
* how i back-up and stuff now with gdrive instead of rclone anymore
* reflash keeb
  * https://docs.keeb.io/assets/files/keymap_Iris_rev5-d4bcf1f19bc0d06c9bd96e9bd73efbd0.pdf

## Formatting Notes

```
one hash title: # title
6 hash image subtitle: ###### subtitle

images: ![]({{site.baseurl}}/assets/2018-04-07-why/post.png)
posts: [previous post]({{site.baseurl}}/2020/01/01/what-i-learned-this-year.html)
links: [display](url)

---
layout: post
title: "post-title"
---
```

## set-up

make the VM
```
vagrant init ubuntu/xenial64
vagrant up
```

change to `root` and update
```
sudo su
apt-get update
```

install packages
```
apt-get install -y ruby-full build-essential zlib1g-dev
gem install jekyll bundler jekyll-import
```

add jekyll to bundle
```
bundle add jekyll
```

## update

clone the repo
```
git clone <repo>
```

update jekyll
```
bundle update jekyll
```

remove any previous cached artifacts
```
bundle exec jekyll clean
```

start the test site locally
```
bundle exec jekyll serve --host <if-ip-addr>
```

## import `wordpress-export.xml`

install the rubygem [jekyll-import](https://import.jekyllrb.com/docs/installation/)
```
$ gem install jekyll-import
```

import the `wordpress-export.xml`
```
$ ruby -r rubygems -e 'require "jekyll-import";
    JekyllImport::Importers::WordpressDotCom.run({
      "source" => "wordpress.xml",
      "no_fetch_images" => false,
      "assets_folder" => "assets"
    })'
```
