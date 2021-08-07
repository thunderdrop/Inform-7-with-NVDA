# Getting the Most out of the Inform 7 Windows IDE with NonVisual Desktop Access

***

## Purpose of this Document

This document exists to familiarize an Inform 7 author with the form and functions of David Kinder's Windows interface, and recommendations of how these can best be accessed with a screen reader. This document primarily focuses on using the program with [NonVisual Desktop Access](https://www.nvaccess.org/) (herein "NVDA"), though some of these techniques have equivalents in other screen readers, and applying those equivalents may have positive results.

#### A Reminder to Sighted Readers

Screen readers are only specialized insofar as they convert on-screen text to speech or Braille output. They do this through calls to existing APIs, which are well documented and officially supported.

### Method

This documentation is split into two sections.

The first discusses the ease of access to the functions of the modern Inform 7 IDE. In this case, "ease" refers not to a user's proficiency with either their screen reader or Inform 7, but the relative accessibility of those functions to NVDA's built-in services.

Most users reasonably familiar with NVDA already have the skills necessary to use Inform 7 with it. For all but the "Story" tab, standard editing and page navigation commands are all you will need. To use the "Story" tab, you will need to know the basics of [object navigation](https://www.nvaccess.org/files/nvda/documentation/userGuide.html#ObjectNavigation) and [text review](https://www.nvaccess.org/files/nvda/documentation/userGuide.html#ReviewingText).

The second section is less organized: It contains specific information on how to work around accessibility bugs in Inform 7 for Windows to accomplish certain tasks. It is only descriptive, and is not intended as a discussion of best practice. In other words, if you find a better way, do that instead. And please share it with us!

## Contributing

If you have comments, corrections, or tips of your own, please submit them in an issue or a pull request.

If you are interested in the workings of Inform 7 for Windows itself, [its sourcecode is here](https://github.com/DavidKinder/Windows-Inform7).

I'm providing the above link in good faith, and not as any kind of dig at David Kinder. He has worked and _does_ work hard on the software, and I don't believe its present state of accessibility to be a result of any malice on his part. I encourage people to open issues and give constructive feedback, but not to go after the guy.

That said, I will not spend any time apologizing for its inaccessibility either. Problems with accessibility are [bugs](https://www.techopedia.com/definition/24864/software-bug-) by definition, and anyone's wanting them fixed is not personal.

***

## Usability

This section discusses the various tasks an Author can acomplish in Inform 7 for Windows, and how much they might be impeded by the program's current design.

The information here applies most specifically to versions of Inform 7 build 6m62, but applies fairly consistently back to build 6g60.

The minimum tested NVDA version is 2014.1. Since the current stable release is version 2021.1, this should be good news for a range of users.

### No Barrier

Most of the core functions of the Inform 7 IDE are thankfully all available to a user of NVDA, with no barrier in the best cases and a slight learning curve in the worst. Here is a complete list of everything that is possible:

* The creation and management of projects
* The creation and management of extensions and extension projects
* Navigation between different parts of the interface
* The writing, reading, and editing of source
* Compilation and release
* The reading of compilation errors
* Searching the Documentation
* The adjustment of preferences

### Low Barrier (Doable, but difficult or inconvenient)

The features in the following list are all technically accessible, but their functionality is diminished to a point where their usability is somewhat debatable. They are also most likely the easiest to fix.

* Viewing the built-in documentation (slightly improved in 64-bit app)
* The reading of highlighted syntax (requires changing NVDA settings)
* Playing or testing projects in the "story" tab
* Using the "Test Me" feature
* Using the spell checker
* Viewing the console output

### High Barrier (Not Currently Possible)

The following features are not currently usable in any meaningful way. These are listed in order of most-to-least trivial to fix.

* The entire index
* The skein
* Navigation or restriction by headings
* Viewing the transcript

***

## Using the Program

What follows is a collection of tips and tricks, in no particular order. They concern potential approaches to working around some of the limitations of the software, listed in the "No" and "Low" Barrier sections. This is not intended to be a technical representation of the issues, but a summary of techniques for an Author wanting to maximize what they can use.

I hope others will contribute their own information to this document, I would love to have missed something.

### Navigating Between Parts of the Window

Various keyboard shortcuts work in Inform which allow you to easily skip between parts of the window. Here are the most useful ones:

<table>
	<tr>
		<th>Press</th>
		<th>To</th>
	</tr>
	<tr>
		<td>CTRL+F1</td>
		<td>view/edit source text</td>
	</tr>
	<tr>
		<td>CTRL+F2</td>
		<td>show compilation report and the console</td>
	</tr>
	<tr>
		<td>CTRL+F6</td>
		<td>Show a running version of compiled source</td>
	</tr>
	<tr>
		<td>CTRL+F7</td>
		<td>Show the documentation</td>
	</tr>
	<tr>
		<td>CTRL+F8</td>
		<td>show installed extensions in-app</td>
	</tr>
	<tr>
		<td>CTRL+F9</td>
		<td>project-specific preferences</td>
	</tr>
</table>

A final shortcut is worth mentioning in this section, and that is the "Switch Panes" shortcut - F6.
Inform 7 remembers the last thing you were doing before using one of the commands in the table above. To switch back to that task, press F6.

e.g. When you compile your source ("Go!") either compilation will succeed and you will be placed on the "Story" tab, or it will fail, and you will be placed in a report containing compilation errors. To switch back to your source from here, you can press F6.

### Other Shortcuts

Inform 7 for Windows also has other shortcuts typical of Windows programs. CTRL+n for "new", CTRL+O for "open", CTRL+S for "save", CTRL+Z for undo, CTRL+F for find, etc. Menus can also be navigated to with alt+accelerator (where accelerator is a letter in the menu's name). A list of these shortcuts is in the next section.

There are a few more built-in keyboard shortcuts specific to Inform 7 projects which make life easier:

<table>
	<tr>
		<th>Press</th>
		<th>To</th>
	</tr>
	<tr>
		<td>F5</td>
		<td>compile and run("Go!")</td>
	</tr>
	<tr>
		<td>F7</td>
		<td>Compile without running ("Refresh Index")</td>
	</tr>
	<tr>
		<td>F10</td>
		<td>find in files</td>
	</tr>
</table>

### The Menu Bar

As of 6m62, the names of the menus on the menu bar are no longer announced after pressing alt. They still behave normally in every other way, but this can throw some people off. Here are the shortcut keys to get to individual menus.

<table>
	<tr>
		<th>Press</th>
		<th>For</th>
	</tr>
	<tr>
		<td>Alt+F</td>
		<td>File</td>
	</tr>
	<tr>
		<td>Alt+E</td>
		<td>Edit</td>
	</tr>
	<tr>
		<td>Alt+O</td>
		<td>Format</td>
	</tr>
	<tr>
		<td>Alt+P</td>
		<td>Play</td>
	</tr>
	<tr>
		<td>Alt+A</td>
		<td>Replay</td>
	</tr>
	<tr>
		<td>Alt+R</td>
		<td>Release</td>
	</tr>
	<tr>
		<td>Alt+W</td>
		<td>Window</td>
	</tr>
	<tr>
		<td>Alt+H</td>
		<td>Help</td>
	</tr>
</table>

### Testing your Game

Inform 7 for Windows has built-in interpreters which will run your compiled code in a console on the "Story" tab, allowing you to test it straight from the IDE without needing to release it for testing every time you make a change. This feature is almost accessible to screen reader users. You will be able to enter commands into your story and read their output, with a caveat:

At present, the output of your commands is not automatically read by a screen reader as it comes in; you will have to manually scroll up each time you enter a command, and read the output line by line.

It comes down to a question of what you find most inconvenient. You can of course release the game and play it in an interpreter which automatically reads the output, but you will have to do that every time you make even the smallest change. If you choose to use the "Story" tab, you will have to read the output manually. This can be frustrating (especially if your testing commands give a lot of output), as each time you enter something, your focus jumps to the bottom of that pane.

Here are some instructions for reading the output from within the app, and some tips to make it a little less painful.

By default, Inform 7 for Windows automatically places your focus where you need it. You will know you are in the right place if you see a multi-line edit with your command prompt in it. This will be ">", or whatever you set it to in your source.

If you aren't placed in the correct field, press CTRL+F6 to get there. If you're not sure that you are there, you can press F6 twice to jump back to the previous pane, and then to the "Story" tab.

From here, you can use basic text review [commands](https://www.nvaccess.org/files/nvda/documentation/userGuide.html#ReviewingText) to view your input and output. These appear in the same field, in the manner of Frotz, Glulx, and HTML TADS.

If your keyboard focus is in the right place but your review cursor is somewhere else, anchor your review cursor to your keyboard focus with the shortcut set on your system. By default, the shortcuts are:

* Desktop layout: NVDA+numpadMinus
* Laptop layout: NVDA+backspace

You may also want to unsync your review cursor from your system caret. This reduces the amount of scrolling up, as new commands will not reset the position of your review cursor to the bottom. The default gesture for this on all layouts is NVDA+6. The gesture is called:

> Toggles on and off the movement of the review cursor due to the caret moving.

If you would rather just run your testing commands from the IDE and view the output somewhere else, you can type them in as defined in source, and then copy the contents of the field to a file.

1. CTRL+A in the console to select all
2. CTRL+C to copy selection.
3. CTRL+V in a file somewhere to paste.

### Reading the Compilation Log

When you compile your source, inform prints some information about that process to another console on the "Results" tab. This is distinct from the "Report", which gives human-readable messages about compilation. This other information can be useful for debugging Inform itself. If something strange happens, information about it will appear here. To access this, do the following:

Ensure you have simple review mode on, and then focus the "Results" tab with CTRL+F2. You will be positioned in the regular compilation report.

Now, set your navigator object to your keyboard focus. NVDA may say "paragraph".

From here, you need to go up by three levels of object containment, so do the gesture you have assigned for this thrice. By default it is NVDA+numpad8 in the desktop layout, Shift+NVDA+up in laptop.

The first time you press the gesture, NVDA will start reading a line from the compilation report. The second time you do it, NVDA will say "table". The third time, NVDA will say "document".

Navigate left from here (NVDA+numpad4 or Shift+NVDA+left) and you will find an unlabelled tab control. Move inside the tab control (NVDA+numpad2 or Shift+NVDA+down) and you will be focused on the 'Report" tab, which will be selected.

Move to the right once (NVDA+numpad6 or Shift+NVDA+right), and you will hear "console  tab". Activate this tab (NVDA+enter), and your keyboard focus will jump into the console Window, which you can navigate with your arrow keys or review cursor as you prefer.

### Notes on Reading Syntax

It is indeed possible to get information on highlighted syntax, if that is important to you. You can set the font and style of certain source elements on the "Editing" tab of the main preferences dialog. This is not the CTRL+F9 preferences, but the one accessed from the "Edit" menu.

At the moment, the Windows color picker seems not to read the names of the preset colors as it used to, so people unfamiliar with RGB or HSL will not be able to set colors for source elements. Setting font style and size works normally.

To get NVDA to read font changes in your source, you will need to enable the following options in NVDA's "Document Formatting" settings.

* Font attributes
* Font style
* Report formatting changes after the cursor

You may also wish to enable line indentation reporting: NVDA can read out the number of spaces or tabs that a line is indented by, or play a tone. The higher the tone, the wider the indent.

If you feel like you may be turning these things on and off frequently, you could create a [configuration profile](https://www.nvaccess.org/files/nvda/documentation/userGuide.html#ConfigurationProfiles) to have NVDA do it for you.

