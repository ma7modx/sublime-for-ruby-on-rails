# sublime-for-ruby-on-rails
sublime settings and packages for ruby on rails development

## install repository and discovery tool for sublime 3
  - copy this command to sublime console 
```
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```
## Packages
  - advancedNewFile
  - sideBarEnhancements
  - git
  - gitGutter
  - closeOtherWindows
  - all AutoCompelete
  - bracketHighlighter
  - beautifyRuby
  - emmet
  - ctags
  - alignment
  - colorPicker
  - railsDeveloperSnippets
  - ruboCop
  - rubyOnRailsSnippets
  - rubyCompletion
  - rubySlim
  - sublimeLitner
  - sublimeRepl

## Settings
  ```
  {
	"auto_complete": true,
	"auto_complete_commit_on_tab": false,
	"bold_folder_labels": true,
	"color_scheme": "Packages/User/SublimeLinter/Monokai (SL).tmTheme",
	"highlight_line": true,
	"highlight_modified_tabs": true,
	"ignored_packages":
	[
		"ASP",
		"C#",
		"C++",
		"Clojure",
		"Go",
		"Groovy",
		"Java",
		"Lisp",
		"Lua",
		"Matlab",
		"Objective-C",
		"Pascal",
		"Perl",
		"PHP",
		"R",
		"Scala",
		"SQL",
		"Vintage"
	],
	"index_files": true,
	"line_padding_bottom": 0.5,
	"line_padding_top": 0.5,
	"new_window_settings":
	{
		"show_minimap": false
	},
	"rulers":
	[
		80,
		120
	],
	"save_on_focus_lost": true,
	"show_definitions": false,
	"tab_size": 2,
	"translate_tabs_to_spaces": true,
	"word_wrap": true
  //"trim_trailing_white_space_on_save": true,
  //"ensure_newline_at_eof_on_save": true
}
  ```

## Key Bindings
  ```
  [
  	{ "keys": ["ctrl+space"], "command": "auto_complete" },
  	{ "keys": ["ctrl+shift+up"], "command":"select_lines", "args": {"forward": false} },
	{ "keys": ["ctrl+shift+down"], "command": "select_lines", "args": {"forward": true} }
  ]
  ```
