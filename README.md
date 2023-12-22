# ISXOgre-Code-Snippets

Getting started:  
1. Set Up Your Development Environment
Install Node.js and npm: These are essential for extension development. You can download them from Node.js website.
Install Visual Studio Code: If you haven't already, download and install VS Code from here.

3. Scaffold Your Extension
Install Yeoman and VS Code Extension Generator: Open a terminal and run:

npm install -g yo generator-code

File Association
Ensure that your .iss file is correctly associated with a language mode that matches the language identifier used in your snippets file. If you're using a workaround language (like JavaScript), set the language mode of the .iss file to that language.
To change the language mode, click on the language indicator in the bottom-right corner of VS Code (it might say "Plain Text") and select the language you've associated with your snippets.
 Correct Syntax in JSON Snippets File

   
Make sure your ogrebasics.json file with the snippets is correctly formatted. Each snippet should be structured as follows:

{
  "SnippetName": {
    "prefix": "yourPrefix",
    "body": [
      "line 1 of your snippet",
      "line 2 of your snippet",
      // more lines as needed
    ],
    "description": "A brief description of what your snippet does"
  }
  // other snippets
}

i've found out with json that it's VERY easy to misplace commas, brackets etc -- so be mindful of what/where you put things as you do them

 Correct Placement of JSON File and loading (for the moment)
   
If you're manually testing snippets, your ogrebasics.json file should be placed in a location where VS Code can recognize it. Normally, snippets are placed within an extension or the user's global snippets directory (File > Preferences > User Snippets).
If you haven't created a full extension, you can try adding your snippets to the global snippets. Go to File > Preferences > User Snippets, then choose New Global Snippets file, and copy your snippets into this file.

Reload VS Code
Sometimes, after making changes to the snippets file or settings, you need to reload VS Code. You can do this by closing and reopening the application, or pressing Ctrl+Shift+P (or Cmd+Shift+P on Mac) and typing 'Reload Window'.


Testing the Snippet
When testing, type the prefix of your snippet in the .iss file and press Tab. If the snippet is recognized, it should expand. -- please use PR's before merging to master 

Checking for Conflicts
Ensure there are no conflicts with other extensions or settings that might interfere with the functioning of snippets.

Language Identifier
If you've created a VS Code extension for these snippets, make sure that the language identifier in your extension's package.json file matches the language you've set for your .iss files.

 Debugging
If the snippets still aren't working, open the Output panel in VS Code (View > Output), and check for any relevant errors or messages that might give clues as to what's going wrong.

Eventually i might look at doing something more "generative code" with file formatting ,but for now snippets are something i'd like to focus on


eventually publishing will happen and we'll go over steps when we get there (hopefully)! 
