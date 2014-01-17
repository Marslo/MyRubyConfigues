RubyTools
=========

The configuration for ruby tools: pry, etc
       Author: Marslo  
        Email: marslo.vida@gmail.com  
   LastChange: 2013-09-03 22:03:02  

## Ruby Tools
### Pry
#### Installation:
- pry:
    <pre><code>gem install pry</code></pre>
- pry-theme:
    <pre><code>gem install pry-theme</code></pre>

#### Usage
- Windows:
    - Copy `.pryrc` and `.pry` from `RubyTools_Config_Marslo\pry` to `%USERPROFILE%`
- Linux:
    - Copy `.pryrc` and `.pry` from `RubyTools_Config_Marslo\pry` to `$HOME`

### RubyMine:
#### Settings:
- Appearance
    - Theme: Darcula
    - Font: Consolas / 12
- Editor
    - Colors & Fonts:
        - Primary Font: Consolas / 18 / 1.0
    - Console Font:
        - Primary Font: Conoslas / 14 / 1.0
#### Reference
- [HomePage](https://github.com/pry/pry)
- [WiKi](https://github.com/pry/pry/wiki)
- [Pry-Theme](https://github.com/kyrylo/pry-theme)

# Installation:

## Ruby by source code
### yaml

    # wget http://pyyaml.org/download/libyaml/yaml-0.1.4.tar.gz
    # tar xzf yaml-0.1.4.tar.gz
    # cd yaml-0.1.4
    # make --prefix=/usr/local
    # make install

### Ruby

    # wget http://ftp.ruby-lang.org/pub/ruby/1.9/ruby-1.9.3-p484.zip
    # unzip ruby-1.9.3-p484.zip
    # cd ruby-1.9.3-p484
    # ./configure --with-opt-dir=/usr/local/lib --enable-shared
    # make && make install

## Ruby Libs

### ruby-openssl
#### Installation

    # cd <RUBY_SOURCE_PAT>/ext/openssl
    # ruby extconf.rb
    # make
    # sudo make install

## Rails Gems
### gem install rmagick

    # apt-get install build-essential imagemagick libmagickcore-dev libmagickwand-dev
    # gem install rmagick

## Q&A Errors&Soluction

### Ruby Enterprise 1.8.7-2012.02
- Error: `make: *** [libtcmalloc_minimal_la-tcmalloc.lo] Error 1`
- Soluction:
    - Download [patch](https://gist.github.com/xibbar/3186499)
    - Run
    <pre><code>$ patch -p1 <PATH_OF_gistfile1.txt>
    $ sudo ./install
    </code></pre>

### Openssl
- Error:
    <pre><code>checking for openssl/ssl.h... no</code></pre>
- Soluction: 
    <pre><code># apt-get install libssl-dev libssl-doc</code></pre>

### Mechanize in windows
- Error 
    <pre><code>ERROR: Failed to build gem native extension
    invalid switch in RUBYOPT: -F (RuntimeError)
    </code></pre>
- Soluction
    -Run commands as below in CMD
    <pre><code>> REG DELETE "HKCU\Software\Microsoft\Command Processor" /v AutoRun</code></pre>

----

- Error: `libxml2 is missing`
- Soluctoin: [Use ruby 1.9.3](http://stackoverflow.com/questions/16898286/error-invalid-switch-in-rubyopt-f-runtimeerror-is-shown-while-install-gems)

### Gem in windows
- Error: `ERROR: Error install <NAME>: The '<NAME>' native gem require installed build tools`
- Soluction:
    - Download and install [Devkit](http://rubyinstaller.org/downloads/)
    - Run `init`, `review` and `install` as below
    <pre><code>> ruby dk.rb init
    [INFO] found RubyInstaller v1.9.3 at C:/ruby193
    Initialization complete! Please review and modify the auto-generated
    'config.yml' file to ensure it contains the root directories to all
    of the installed Rubies you want enhanced by the Devkit
    > ruby dk.rb review
    Based upon seetings in the 'config.yml' file generated
    from running 'ruby dk.rb init' and any of your customizations,
    DevKit functionlity will be injected into the following Rubies
    when you run 'ruby dk.rb install'.
    > ruby dk.rb install
    [INFO] Updating convenience notice gem override fro 'C:/Ruby193'
    [INFO] Installing 'C:/Ruby193/lib/ruby/site_ruby/devkit.rb'
    </code></pre>

### Change Gem source
#### Commands

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

#### Note
- Basic command: `gem source`
- `-l`: list
- `-r`: remove
- `-a`: add
- `-u`: update

