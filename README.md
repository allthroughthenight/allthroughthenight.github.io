# allthroughthenight.github.io

## TODOs

* All-in-one command to set up VM (Ansible, Vagrant)
* Better understanding overall of static site generators and less-copy-pasta of commands (ಠ_ಠ)
* Fix inline HTML for YouTube videos and images, proabably best to move 'locally' to assets as possible
* Remove unneeded features (RSS Feed, SEO, Google Analytics)
* Use a custom domain
* Clean up git log to one initial 'hero' commit
* Other pages for "About Me" and "Portfolio" maybe?

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
