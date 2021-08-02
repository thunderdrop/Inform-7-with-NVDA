# Getting the Most out of the Inform 7 Windows IDE using NonVisual Desktop Access

***

## Purpose of this Document

This document exists to familiarize an Inform 7 author with the form and functions of David Kinder's Windows interface, and recommendations of how these can best be accessed with a screenreader. This document primarily focuses on using the program with [NonVisual Desktop Access](https://www.nvaccess.org/) (herein "NVDA"), though some of these techniques have equivalents in other screenreaders, and applying those equivalents may have positive results.

### A reminder to sighted readers

Screenreaders are only specialized insofar as they convert on-screen text to speech or Braille output. They do this through calls to existing APIs, which are well documented and officially supported.

### Method

This documentation is split into two sections.

The first discusses the ease of access to the functions of the modern Inform 7 IDE. In this case, "ease" refers not to a user's proficiency with either their screenreader or Inform 7, but the relative accessibility of those functions to NVDA's built-in services.

Most users reasonably familiar with NVDA already have the skills necessary to use Inform 7 with it. For all but the story tab, standard editing and page navigation commands are all you will need. To use the story tab, you will need to know the basics of object navigation.

The second section is less organized: It contains specific information on how to work around accessibility bugs in Inform 7 to acomplish certain tasks. It is only descriptive, and is not intended as a discussion of best practice. In other words, if you find a better way, do that instead. And please share it with us!

## Contributing

If you have comments, corrections, or tips of your own, please submit them in an issue or a pull request.

If you are interested in the workings of the Inform 7 Windows IDE, [its sourcecode is here](https://github.com/DavidKinder/Windows-Inform7).

I'm providing the above link in good faith, and not as a dig at David Kinder. He has worked and does work hard on the software, and I don't believe its present state of accessibility to be a result of any malice on his part. That said, I will not spend any time apologizing for its present state either. Problems with accessibility are [bugs](https://www.techopedia.com/definition/24864/software-bug-) by definition, and anyone's wanting them fixed is not personal.

***

## Usability

This section discusses the various tasks an Author can acomplish in Inform 7, and how much they might be impeded by the program's current design.

The information here applies most specifically to versions of Inform 7 build 6m62, but applies fairly consistently back to build 6g60.

The minimum tested NVDA version is 2014.1. Considering the current stable release is version 2021.1, this should be good news for a range of users.

### No Barrier

Most of the core functions of the Inform 7 IDE are thankfully all available to a user of NVDA, with no barrier in the best cases and a slight learning curve in the worst. Here is a complete list of everything that is possible:

* The creation and management of projects
* The creation and management of extensions and extension projects
* Navigation between different parts of the interface
* The writing, reading, and editing of source
* The reading of highlighted syntax (requires changing NVDA settings)
* Compilation and release
* The reading of compilation errors
* Searching the Documentation
* The adjustment of preferences

### Low Barrier (Doable, but difficult or inconvenient)

The features in the following list are all technically accessible, but their functionality is diminished to a point where their usability is somewhat debatable. They are also most likely the easiest to fix.

* Viewing the built-in documentation (improved in 64-bit app)
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

### Navigating Between Parts of the Window

Various keyboard shortcuts work in Inform which allow you to easily skip between parts of the window. Here are the most useful ones:

<table>
	<tr>
		<th>Press</th>
		<th>To</th>
	</tr>
	<tr>
		<td>CTRL+F1</td>
		<td>source text</td>
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
		<td>preferences</td>
	</tr>
	<tr>
		<td>F10</td>
		<td>find in files</td>
	</tr>
</table>

A final shortcut is worth mentioning in this section, and that is the "Switch Panes" shortcut:
Inform 7 remembers the last thing you were doing before using one of the commands in the table above. TO switch back to that task, press F6.

e.g. When you compile your source ("Go!") either compilation will succeed and you will be placed on the "Story" tab, or it will fail, and you will be placed in a report containing compilation errors. To switch back to your source from here, you can press F6.

