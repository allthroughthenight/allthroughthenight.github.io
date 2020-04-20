# allthroughthenight.github.io

## TODOs

* All-in-one command to set up VM (Ansible, Vagrant)
* Better understanding overall of static site generators and less-copy-pasta of commands (ಠ_ಠ)
* Convert 'What I've Learned So Far' and 'What I've Learned in 2020' to pure Markdown
* Convert scattered inline HTML to pure Markdown
* Close out [WordPress.com](ramblevalley.wordpress.com) site and account
* Remove unneeded features (RSS Feed, SEO, Google Analytics)
* Use my own personal domain

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
bundle exec jekyll serve --host <eth1>
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