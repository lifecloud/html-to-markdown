# Change Log
All notable changes to this project will be documented in this file.
Updates should follow the [Keep a CHANGELOG](http://keepachangelog.com/) principles.

## [Unreleased][unreleased]

### Fixed
 - Added escaping to avoid * and _ in a text being rendered as emphasis (#48)

## [4.0.0]

This release changes the visibility of several methods/properties. #42 and #43 brought to light that some visiblities were
not ideally set, so this releases fixes that. Moving forwards this should reduce the chance of introducing BC-breaking changes.

### Added
 - Added new `HtmlConverter::getEnvironment()` method to expose the `Environment` (#42, #43)

### Changed
 - Changed `Environment::addConverter()` from `protected` to `public`, enabling custom converters to be added (#42, #43)
 - Changed `HtmlConverter::createDOMDocument()` from `protected` to `private`
 - Changed `Element::nextCached` from `protected` to `private`
 - Made the `Environment` class `final`

## [3.1.1]
### Fixed
 - Empty HTML strings now result in empty Markdown documents (#40, #41)

## [3.1.0]
### Added
 - Added new `equals` method to `Element` to check for equality

### Changes
 - Use Linux line endings consistently instead of plaform-specific line endings (#36)

### Fixed
 - Cleaned up code style

## [3.0.0]
### Changed
 - Changed namespace to `League\HTMLToMarkdown`
 - Changed packagist name to `league/html-to-markdown`
 - Re-organized code into several separate classes
 - `<a>` tags with identical href and inner text are now rendered using angular bracket syntax (#31)
 - `<div>` elements are now treated as block-level elements (#33)

## [2.2.2]
### Added
 - Added support for PHP 5.6 and HHVM
 - Enabled testing against PHP 7 nightlies
 - Added this CHANGELOG.md

### Fixed
 - Fixed whitespace preservation between inline elements (#9 and #10)

## [2.2.1]
### Fixed
 - Preserve placeholder links (#22)

## [2.2.0]
### Added
 - Added CircleCI config

### Changed
 - `<pre>` blocks are now treated as code elements

### Removed
 - Dropped support for PHP 5.2
 - Removed incorrect README comment regarding `#text` nodes (#17)

## [2.1.2]
### Added
 - Added the ability to blacklist/remove specific node types (#11)

### Changed
 - Line breaks are now placed after divs instead of before them
 - Newlines inside of link texts are now removed
 - Updated the minimum PHPUnit version to 4.*

## [2.1.1]
### Added
 - Added options to customize emphasis characters

## [2.1.0]
### Added
 - Added option to strip HTML tags without Markdown equivalents
 - Added `convert()` method for converter reuse
 - Added ability to set options after instance construction
 - Documented the required PHP extensions (#4)

### Changed
 - ATX style now used for h1 and h2 tags inside blockquotes

### Fixed
 - Newlines inside blockquotes are now started with a bracket
 - Fixed some incorrect docblocks
 - `__toString()` now returns an empty string if input is empty
 - Convert head tag if body tag is empty (#7)
 - Preserve special characters inside tags without md equivalents (#6)


## [2.0.1]
### Fixed
 - Fixed first line indentation for multi-line code blocks
 - Fixed consecutive anchors get separating spaces stripped (#3)

## [2.0.0]
### Added
 - Initial release

[unreleased]: https://github.com/thephpleague/html-to-markdown/compare/4.0.0...master
[4.0.0]: https://github.com/thephpleague/html-to-markdown/compare/3.1.1...4.0.0
[3.1.1]: https://github.com/thephpleague/html-to-markdown/compare/3.1.0...3.1.1
[3.1.0]: https://github.com/thephpleague/html-to-markdown/compare/3.0.0...3.1.0
[3.0.0]: https://github.com/thephpleague/html-to-markdown/compare/2.2.2...3.0.0
[2.2.2]: https://github.com/thephpleague/html-to-markdown/compare/2.2.1...2.2.2
[2.2.1]: https://github.com/thephpleague/html-to-markdown/compare/2.2.0...2.2.1
[2.2.0]: https://github.com/thephpleague/html-to-markdown/compare/2.1.2...2.2.0
[2.1.2]: https://github.com/thephpleague/html-to-markdown/compare/2.1.1...2.1.2
[2.1.1]: https://github.com/thephpleague/html-to-markdown/compare/2.1.0...2.1.1
[2.1.0]: https://github.com/thephpleague/html-to-markdown/compare/2.0.1...2.1.0
[2.0.1]: https://github.com/thephpleague/html-to-markdown/compare/2.0.0...2.0.1
[2.0.0]: https://github.com/thephpleague/html-to-markdown/compare/775f91e...2.0.0

