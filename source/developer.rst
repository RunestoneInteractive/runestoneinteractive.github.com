Developer Documentation for Runestone Interactive Tools
=======================================================

The Runestone system uses `ReStructured Text <http://docutils.sourceforge.net/rst.html>`__ (.rst) as its primary markup language.
ReStructuredText is easy to read in plain text form, and can be transformed into 
html, latex, epub, or our own interactive book format.
Runestone is built on top of `Sphinx <http://www.sphinx-doc.org/en/master/>`__,
so any markup valid in `ReStructured Text <http://docutils.sourceforge.net/rst.html>`__ 
or `Sphinx <http://www.sphinx-doc.org/en/master/>`__
is also valid in Runestone.


Important Notes
---------------

- We do our development on Linux and OS X.
  We use standard Unix commands that may not exist on Windows.
  If you want to install on Windows, you may need to install the
  Cygwin tools and do your work in that environment.

- Books should compile easily on any environment where sphinx installs and runs.

- Developers who desire to add new components to Runestone, or
  modify the Runestone server, should consider developing on Ubuntu 16.10.
  Tests that run within the Selenium test automation framework should
  *theoretically* run anywhere it installs, however, some 
  versions appear to be more forgiving than others.

Development Parts
-----------------

If you plan to develop on the Runestone project,
you should know that there are now **three pieces** of a **local Runestone development environment.**

1. The `Runestone Components <https://github.com/RunestoneInteractive/RunestoneComponents>`_ -
   this is the development version of the library you get when you ``pip install runestone``.
   *You should examine this first.*
   See the `components GitHub repository <https://github.com/RunestoneInteractive/RunestoneComponents>`__,
   where the README is approximately up to date.
   If you are *only* interested in authoring content and/or developing directives
   (extensions to ReStructuredText that provide interactive components of textbooks), you only need this.
   (You may also want open source book content to edit -- see #3. You can skip #2.)

2. The `Runestone Server <https://github.com/RunestoneInteractive/RunestoneServer>`_ -
   this is the application that goes inside a **web2py** server.
   If you plan to run your own server for an interactive textbook,
   or develop on the Runestone server, you should install this.
   See the `server GitHub repository <https://github.com/RunestoneInteractive/RunestoneServer>`__,
   where the README is approximately up to date.

3. **A book** written for the runestone environment to build, deploy, and then serve on your local server.
   Typically, a book repository will be cloned (and potentially edited) 
   to the appropriate place inside the Runestone server application, 
   and can be built using the tools provided by RunestoneComponents. 
   You can see an example of a book created for the Runestone environment on 
   GitHub `here <https://github.com/RunestoneInteractive/thinkcspy>`_. 
   See the `RunestoneComponents README <https://github.com/RunestoneInteractive/RunestoneComponents>`__
   for how to build and serve the book content locally.

Note that if you intend *solely* to be a content author and *not* to do any 
code development for the Runestone project, 
you should look at the RunestoneComponents repository only.

The `Runestone organization <https://github.com/RunestoneInteractive>`_ 
on Github provides access to every GitHub repository managed by RunestoneInteractive.

**NOTE: This documentation is currently undergoing significant updates. If you wish to develop on the Runestone project, please see the above links.**


Using Special Runestone Extensions
----------------------------------

Runestone includes all of the pre-existing `ReStructured Text <http://docutils.sourceforge.net/rst.html>`__ 
formatting -- you can use the documentation there for syntax guidance, 
for example: formatting like **bold** or *italic*, adding hyperlinks, tables, figures, formulas, etc. 
Runestone extends `Sphinx <http://www.sphinx-doc.org/en/master/>`__ with several custom 
ReStructured Text *directives*. 
**Directives** allow you to include special interactive elements in a page.
Runestone directives include video, images, working with source code in the browser, 
adding interactive exercises, and more.
The Runestone directives documentation includes full documentation of all of the available Runestone directives,
including:

* What each directive allows you to create
* The syntax for using each directive
* Examples, or links to examples, of how instructors have used these directives in interactive textbook work
* If applicable, how exercises created by these directives can be graded
* Available additional developer documentation for each directive

