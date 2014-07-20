# The PHP Specification

Quoting [`php.net`](http://php.net):

> PHP is a popular general-purpose scripting language that is especially suited
> to web development.
> 
> Fast, flexible and pragmatic, PHP powers everything from your blog to the most
> popular websites in the world.

PHP is a multiparadigm scripting language. It is interpreted by a virtual
machine.

## Why a specification?

Since the beginning, [the `php-src` virtual machine](http://php.net/), was the
only one on the market. Today, we see several others, like
[HHVM](http://hhvm.com/), [Phalanger](https://github.com/DEVSENSE/Phalanger),
[JPHP](https://github.com/jphp-compiler/jphp), [HippyVM](http://hippyvm.com/)
etc. Having a “reference implementation”, aka `php-src` is [no longer suitable
for the future of PHP](http://marc.info/?l=php-internals&m=139565259319206):

  * the reference implementation can contain bugs, consequently, the PHP
    language contains bugs,
  * the version of the reference implementation must not be the same that the
    one of the language,

Thus, we propose to write a PHP Specification. First, the PHP Specification will
describe the PHP language. All other features implemented by one or another
virtual machine will not be a feature of the PHP language. Second, the (new)
[RFC platform](http://wiki.php.net/rfc/) allows to describe potential new
features (not necessarily implemented in `php-src`). Now, this platform must be
a central platform for all virtual machines. (Anecdotally, comparisons of
virtual machines must be based on the PHP Specification).

# Content of the specification

The specification is composed of several chapters:

  1. Introduction
  2. Lexical structure
  3. Type system
  4. Statements and expressions
  5. Functions
  6. Classes, interfaces and traits
  7. Namespaces
  8. Memory
  9. Execution model
