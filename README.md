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
## Plugins
  to create a plugin ```Tools-> Developer-> Plugin```
  - CloseOthersCommand
  ```
import sublime_plugin

class CloseOthersCommand(sublime_plugin.TextCommand):
    def run(self, edit):
        window = self.view.window()
        group_index, view_index = window.get_view_index(self.view)
        window.run_command("close_others_by_index", { "group": group_index, "index": view_index})
	```
  - CloseToRightCommand
  ```
import sublime_plugin

class CloseToRightCommand(sublime_plugin.TextCommand):
    def run(self, edit):
        window = self.view.window()
        group_index, view_index = window.get_view_index(self.view)
        window.run_command("close_to_right_by_index", { "group": group_index, "index": view_index})
	```
  - to add these plugins in the key bindings 
  
 ```
 { "keys": ["ctrl+shift+w"], "command": "close_others" }
 { "keys": ["ctrl+shift+e"], "command": "close_to_right" }
 ```
 ## Global Configurations
 to edit global configurations ```git config --global -e```
	
  ```
	  [alias]
		tree = log --graph --oneline --decorate --branches --all
		treeme = log --graph --oneline --decorate
		treea = log --graph --pretty=short --decorate --branches --all
		treemea = log --graph --pretty=short --decorate 
		treeadv = log --all --graph --decorate --branches --format='%C(cyan) %p %Cred %h %C(white) %s %C(cyan) <%an>%C(bold yellow)%d%Creset'
		treemeadv = log --graph --decorate --format='%C(cyan) %p %Cred %h %C(white) %s %C(cyan) <%an>%C(bold yellow)%d%Creset'
```
  

