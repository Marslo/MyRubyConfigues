RubyTools
=========

The configuration for ruby tools: pry, etc
       Author: Marslo  
        Email: marslo.vida@gmail.com  
   LastChange: 2013-09-03 22:03:02  

# Pry
## Installation:
- pry:
       <pre><code>gem install pry</code></pre>
- pry-theme:
       <pre><code>gem install pry-theme</code></pre>

## Usage
- Windows:
    - Copy `.pryrc` and `.pry` from `RubyTools_Config_Marslo\pry` to `%USERPROFILE%`
- Linux:
    - Copy `.pryrc` and `.pry` from `RubyTools_Config_Marslo\pry` to `$HOME`

# RubyMine:
## Settings:
- Appearance
    - Theme: Darcula
    - Font: Consolas / 12
- Editor
    - Colors & Fonts:
        - Primary Font: Consolas / 18 / 1.0
    - Console Font:
        - Primary Font: Conoslas / 14 / 1.0

## Reference
- [HomePage](https://github.com/pry/pry)
- [WiKi](https://github.com/pry/pry/wiki)
- [Pry-Theme](https://github.com/kyrylo/pry-theme)

# Rails Gems
## gem install rmagick

    # apt-get install build-essential imagemagick libmagickcore-dev libmagickwand-dev
    # gem install rmagick

## Change source
### Commands

    $ gem source -l
    *** CURRENT SOURCES ***
    http://rubygems.org
    $ gem source -r http://rubygems.org/
    source http://rubygems.org not present in cache
    $ gem source -l
    *** CURRENT SOURCES ***
    $ gem source -a http://ruby.taobao.org
    http://ruby.taobao.org added to sources
    $ gem source -u
    source cache successfully updated
    $ gem source -l
    *** CURRENT SOURCES ***
    http://ruby.taobao.org

### Note
- Basic command: `gem source`
- `-l`: list
- `-r`: remove
- `-a`: add
- `-u`: update

## Install ruby-openssl by manual
### Installation
<pre><code># cd <RUBY_SOURCE_PAT>/ext/openssl
    # ruby extconf.rb
    # make
    # sudo make install
</code></pre>
### Errors
- `checking for openssl/ssl.h... no`
- `# apt-get install libssl-dev libssl-doc`
