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
<pre><code>apt-get install build-essential imagemagick libmagickcore-dev libmagickwand-dev</code></pre>

## Change source

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

