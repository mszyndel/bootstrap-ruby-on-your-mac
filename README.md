bootstrap-ruby-on-your-mac
==========================

Fast and easy way to set up Ruby/Rails env on your mac with gem separation

Purpose
--------------------------
I wanted to setup my development environment to have automatic gem separation while being independent of Ruby version or installation method (Homebrew, rbenv, RVM)
I dislike RVM gemsets concept because you need to create and manage them manually.

Steps
--------------------------
Given you have just MacOS bundled Ruby do the following. If you have your favourite Ruby already installed, skip steps 1-3
1. Install homebrew  
```
ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
```
2. Install Ruby of choice  
```
brew install ruby
```  
or for 1.9.3  
```
  brew tap homebrew/versions
  brew install homebrew/versions/ruby193
```
3. Install bundler & rails (just in case you'd like to do ```rails new```)  
```
gem install bundler rails
```
4. Add following line to your ```~/.bash_login```  
```
export BUNDLE_PATH=.gems/
```
5. Install https://github.com/gma/bundler-exec

Voila!

Now each Rails project will have it's own gems installed in $PROJECT_PATH/.gems directory
