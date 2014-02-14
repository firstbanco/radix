# Radix

This is a patch of the excellent radix gem to support Ruby 2.1.

Radix: http://rubyworks.github.com/radix
Ruby 2.1 issue: https://github.com/rubyworks/radix/issues/10

You can use it as before thus:

    gem 'radix-firstbanco'

Unfortunately, the release of Ruby 2.1 came with new methods on String "b".  http://www.ruby-doc.org/core-2.1.0/String.html#method-i-b
This clashes with the radix gem.

To use radix-firstbanco, just replace

    123.b(10)

With:

    Radix::Integer.new(123, 10)

When the issue is resolved more formally, this gem will be dissolved.