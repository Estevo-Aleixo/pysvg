pySVG - Creating SVG with python
================================

pySVG is a pure Python library to create SVG documents. Essentially it is a python wrapper around svg with the goal to allow people to "program svg". pySVG can be used to produce svg as an outcome of algorithms you implement (like koch curves, Lindenmayr systems etc.)

Working with pySVG is pretty straightforward. There is a small tutorial in the docs folder but I would suggest refering to the testclasses in the source.

Current status:
---------------

Pretty much all elements should be implemented.
Type checking, validation and value constraints are NOT.

In short: currently you can fill any element with more or less any content. Loading and storing of SVG images also works.

Features
--------

* Shapes (circle, ellipses, rectangles, lines, polygons, polylines,paths)
* Text
* Containers (g-element, defs)
* Style attributes (stroke, filling, font)
* Transform (in groups)
* Filters
* Load/Store SVG files

License & Donation
------------------

BSD - Style:

    Copyright (c) 2008-2012, Kerim Mansour
    
    All rights reserved.
    
    Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
    * Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
    * Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
    
    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
    
    The views and conclusions contained in the software and documentation are those of the authors and should not be interpreted as representing official policies, either expressed or implied, of the FreeBSD Project.
    
    If you enjoy using pySVG, please considering making a small [donation](http://codeboje.de/donate/) to support further development. See the [Donation](http://codeboje.de/donate/) page for more information.


Downloads
---------

pySVG can be found here:

latest [sources](https://github.com/Estevo-Aleixo/pysvg/)

latest [release](https://github.com/Estevo-Aleixo/pysvg/releases) (usually somewhat older, either as dist or with docs and examples)

Acknowledgements
----------------

SVG is a huge format. Some things Kerim Mansour has tested, some he "thinks to have" implemented but didn't test and others haven't been implement yet or only made stubs.

I can't possibly test it all and frankly I am not really a graphics guru.

So I will list anybody here who provides me with code testing yet untested but theoretically implemented features.

So if you happen to create any image using pySVG and the code contains elements and attributes that haven't been tested yet, I would gladly include you in the acknoledgements list along with the "feature" you determined to work correctly.

Installation and Requirements
------------------------------

pySVG requires Python (it was written for version 2.6, other versions may or may not work). pySVG also requires ... nothing else :-)

Releases/History
----------------

    10/12/2010 Release 5 : Version 0.2.1:
    Added
    * added **kwargs to make life a bit easier when instantiating objects
    * added dropshadows (contributed by Bastian)
    * added patterns
    * added turtle graphics
    * added clip element
    * added use element
    * added some methods to get size/edge points or move an element (depends on element)
    * implemented feMergeNode subclassing
    * added filterprimitiveswithin
    Corrections
    * setfilter had wrong parameter
    * corrected intendation
    * documentation corrected
    
    09/29/2009 Release 4 : Version 0.2.0:
    * Complete rewrite of the class hirarchy (multiple inheritance)
    * most if not all all elements should exist now
    * gradients supported
    * filters supported
    * added Parser that loads svg structures into python
    TODO:
    * type and content validation (lower priority)
    * better usage of defs and use commands (higher priority)
    * rewrite this post and bring it up to date ;)
    
    02/27/2009 Release 3 : Version 0.1.6:
    * Path now supported (although not optimized)
    * lineto (horizontal/vertical/free)
    * moveto
    * cureveto (cubic, quadratic, closecurve)
    * arc
    * included epidoc (still much to document though)
    
    02/02/2008 Release 2 : Version 0.1.5:
    * Extracted ObjectHelper
    * style is now a dictionary instead of a class.
    * included transforms (rotation tested so far)
    * for style and transforms i created some Helperclass to create the dicts for those that do not know the attribute names
    * included a "benchmark" now. Just compare the svg here to the created one to see what still is missing as features.
    * broke the tutorial, see the testcode.
    
    01/29/2008 Release 1 : Version 0.1:
    * Basic features work. You can draw circles, ellipses, rectangles, lines, polylines and polygones. Filled and empty with different fill colors, stroke colors and stroke widths.
    * Documentation is under way
    * setup.py should work
    * Not working is all the fancy stuff like transforms, gradients, ids etc.
    * Not working Style attributes not mentioned above MAY already work, haven't tested them all yet.
    * If YOU want to test see "Acknowledgments" above.
