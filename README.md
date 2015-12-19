Rouge::Lexers::Docker
===================

* [Homepage](https://rubygems.org/gems/rouge-lexers-docker)
* [Documentation](http://rubydoc.info/gems/rouge-lexers-docker/frames)
* [Email](mailto:KitaitiMakoto at gmail.com)

Description
-----------

Rouge lexer for Dockerfiles.

Features
--------

Parses and markups Dockerfiles.

Examples
--------

    require 'rouge'
    require 'rouge/lexers/docker'
    
    dockerfile = ARGV.shift
    abort 'USAGE: ruby rougify-dockerfile.rb DOCKERFILE' unless dockerfile
    
    content = File.read(dockerfile)
    lexer = Rouge::Lexers::Docker.new
    lexed = lexer.lex(content)
    
    formatter = Rouge::Formatters::Terminal256.new
    # or formatter = Rouge::Formatters::HTML.new(wrap: false)
    highlighted = formatter.format(lexed)
    print highlighted

Requirements
------------

[Rouge][] gem.

[Rouge]: https://github.com/jneen/rouge

Install
-------

    $ gem install rouge-lexers-docker

Copyright
---------

Copyright (c) 2015 KITAITI Makoto

See COPYING.txt for details.
