
By default, jazzy looks for a file named ".jazzy.yaml" in the source
directory and its ancestors. You can override the config file location
with --config.

(The source directory is the current working directory by default.
You can override that with --source-directory.)

The config file can be in YAML or JSON format. Available options are:


OUTPUT

  Config file:   output
  Command line:  -o, --output FOLDER

  Folder to output the HTML docs to
  Default: docs

CLEAN

  Config file:   clean
  Command line:  -c, --[no-]clean

  Delete contents of output directory before running. 
  WARNING: If --output is set to ~/Desktop, this will delete the ~/Desktop directory.

OBJC MODE

  Config file:   objc
  Command line:  --[no-]objc

  Generate docs for Objective-C.

UMBRELLA HEADER

  Config file:   umbrella_header
  Command line:  --umbrella-header PATH

  Umbrella header for your Objective-C framework.

FRAMEWORK ROOT

  Config file:   framework_root
  Command line:  --framework-root PATH

  The root path to your Objective-C framework.

SDK

  Config file:   sdk
  Command line:  --sdk [iphone|watch|appletv][os|simulator]|macosx

  The SDK for which your code should be built.
  Default: macosx

HIDE DECLARATIONS

  Config file:   hide_declarations
  Command line:  --hide-declarations [objc|swift] 

  Hide declarations in the specified language. Given that generating Swift docs only generates Swift declarations, this is useful for hiding a specific interface for either Objective-C or mixed Objective-C and Swift projects.

CONFIG FILE

  Config file:   config
  Command line:  --config PATH

  Configuration file (.yaml or .json)
  Default: .jazzy.yaml in source directory or ancestor

BUILD TOOL ARGUMENTS

  Config file:   build_tool_arguments
  Command line:  -b, --build-tool-arguments arg1,arg2,…argN

  Arguments to forward to xcodebuild, swift build, or sourcekitten.
  Default: []

XCODEBUILD ARGUMENTS

  Config file:   xcodebuild_arguments
  Command line:  -x, --xcodebuild-arguments arg1,arg2,…argN

  Back-compatibility alias for build_tool_arguments.

SOURCEKITTEN SOURCEFILE

  Config file:   sourcekitten_sourcefile
  Command line:  -s, --sourcekitten-sourcefile filepath1,…filepathN

  File(s) generated from sourcekitten output to parse

SOURCE DIRECTORY

  Config file:   source_directory
  Command line:  --source-directory DIRPATH

  The directory that contains the source to be documented
  Default: /Users/muis/Documents/go-workspace/src/github.com/muizidn/todo-ios

EXCLUDED FILES

  Config file:   exclude
  Command line:  -e, --exclude filepath1,filepath2,…filepathN

  Source file pathnames to be excluded from documentation. Supports wildcards.
  Default: []

INCLUDED FILES

  Config file:   include
  Command line:  -i, --include filepath1,filepath2,…filepathN

  Source file pathnames to be included in documentation. Supports wildcards.
  Default: []

SWIFT VERSION

  Config file:   swift_version
  Command line:  --swift-version VERSION


SWIFT BUILD TOOL

  Config file:   swift_build_tool
  Command line:  --swift-build-tool spm | xcodebuild

  Control whether Jazzy uses Swift Package Manager or xcodebuild to build the module to be documented.  By default it uses xcodebuild if there is a .xcodeproj file in the source directory.

AUTHOR NAME

  Config file:   author
  Command line:  -a, --author AUTHOR_NAME

  Name of author to attribute in docs (e.g. Realm)

AUTHOR URL

  Config file:   author_url
  Command line:  -u, --author_url URL

  Author URL of this project (e.g. https://realm.io)

MODULE NAME

  Config file:   module
  Command line:  -m, --module MODULE_NAME

  Name of module being documented. (e.g. RealmSwift)

VERSION

  Config file:   module_version
  Command line:  --module-version VERSION

  Version string to use as part of the the default docs title and inside the docset.
  Default: 1.0

TITLE

  Config file:   title
  Command line:  --title TITLE

  Title to display at the top of each page, overriding the default generated from module name and version.

COPYRIGHT

  Config file:   copyright
  Command line:  --copyright COPYRIGHT_MARKDOWN

  copyright markdown rendered at the bottom of the docs pages

README PATH

  Config file:   readme
  Command line:  --readme FILEPATH

  The path to a markdown README file

DOCUMENTATION GLOB

  Config file:   documentation
  Command line:  --documentation GLOB

  Glob that matches available documentation

ABSTRACT GLOB

  Config file:   abstract
  Command line:  --abstract GLOB

  Glob that matches available abstracts for categories

PODSPEC

  Config file:   podspec
  Command line:  --podspec FILEPATH

  A CocoaPods Podspec that describes the Swift library to document

DOCSET ICON

  Config file:   docset_icon
  Command line:  --docset-icon FILEPATH


DOCSET PATH

  Config file:   docset_path
  Command line:  --docset-path DIRPATH

  The relative path for the generated docset

ROOT URL

  Config file:   root_url
  Command line:  -r, --root-url URL

  Absolute URL root where these docs will be stored

DASH URL

  Config file:   dash_url
  Command line:  -d, --dash_url URL

  Location of the dash XML feed e.g. https://realm.io/docsets/realm.xml)

GITHUB URL

  Config file:   github_url
  Command line:  -g, --github_url URL

  GitHub URL of this project (e.g. https://github.com/realm/realm-cocoa)

GITHUB FILE PREFIX

  Config file:   github_file_prefix
  Command line:  --github-file-prefix PREFIX

  GitHub URL file prefix of this project (e.g. https://github.com/realm/realm-cocoa/tree/v0.87.1)

DISABLE SEARCH

  Config file:   disable_search
  Command line:  --disable-search

  Avoid generating a search index. Search is available in some themes.

SKIP DOCUMENTATION

  Config file:   skip_documentation
  Command line:  --skip-documentation

  Will skip the documentation generation phase.

MIN ACL

  Config file:   min_acl
  Command line:  --min-acl [private | fileprivate | internal | public | open]

  minimum access control level to document
  Default: public

SKIP UNDOCUMENTED

  Config file:   skip_undocumented
  Command line:  --[no-]skip-undocumented

  Don't document declarations that have no documentation comments.

HIDE DOCUMENTATION COVERAGE

  Config file:   hide_documentation_coverage
  Command line:  --[no-]hide-documentation-coverage

  Hide "(X% documented)" from the generated documents

CUSTOM CATEGORIES

  Config file:   custom_categories

  Custom navigation categories to replace the standard “Classes, Protocols, etc.”
  Types not explicitly named in a custom category appear in generic groups at the end.
  Example: https://git.io/v4Bcp
  Default: []

CUSTOM CATEGORIES UNLISTED PREFIX

  Config file:   custom_categories_unlisted_prefix

  Prefix for navigation section names that aren't explicitly listed in `custom_categories`.
  Default: Other 

HIDE UNLISTED DOCUMENTATION

  Config file:   hide_unlisted_documentation
  Command line:  --[no-]hide-unlisted-documentation

  Don't include documentation in the sidebar from the `documentation` config value that aren't explicitly listed in `custom_categories`.

CUSTOM HEAD

  Config file:   head
  Command line:  --head HTML

  Custom HTML to inject into <head></head>.

THEME DIRECTORY

  Config file:   theme
  Command line:  --theme [apple | fullwidth | jony | DIRPATH]

  Which theme to use. Specify either 'apple' (default), one of the other built-in theme names, or the path to your mustache templates and other assets for a custom theme.
  Default: apple

USE SAFE FILENAMES

  Config file:   use_safe_filenames
  Command line:  --use-safe-filenames

  Replace unsafe characters in filenames with an encoded representation. This will reduce human readability of some URLs, but may be necessary for projects that expose filename-unfriendly functions such as /(_:_:)

TEMPLATE DIRECTORY

  Config file:   template_directory
  Command line:  -t, --template-directory DIRPATH

  DEPRECATED: Use --theme instead.

ASSETS DIRECTORY

  Config file:   assets_directory
  Command line:  --assets-directory DIRPATH

  DEPRECATED: Use --theme instead.

UNDOCUMENTED TEXT

  Config file:   undocumented_text
  Command line:  --undocumented-text UNDOCUMENTED_TEXT

  Default text for undocumented symbols. The default is "Undocumented", put "" if no text is required
  Default: Undocumented
