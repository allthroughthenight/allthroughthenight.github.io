# allthroughthenight.github.io

A basic blog for my basic post, all views are my own.

## TODOs

* All-in-one VM set-up via Ansible and Vagrant
* Better understanding of overall static site generators and less-copy-pasta of commands (ಠ_ಠ)
* Change pics back to direct links since they're not gonna be embedded/inline

## Formatting Notes

```
one hash title: # title
6 hash image subtitle: ###### subtitle

images: ![]({{site.baseurl}}/assets/2018-04-07-why/post.png)
posts: [previous post]({{site.baseurl}}/2020/01/01/what-i-learned-this-year.html)
links: [display](url)
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
