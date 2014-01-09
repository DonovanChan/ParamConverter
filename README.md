# ParamConverter

Converting dictionary formats in FileMaker Pro

## Overview

As outlined here, ModularFileMaker.org suggests using “Let Variables” for passing named parameters to scripts. This method for constructing name-value pairs is popular in large part because it leverages native functionality and doesn’t require any custom functions.

### Let Format

````
"$name = \"Calvin\" ;
$age = 5 ;"
````

### SFR Format

Still, others prefer to use alternative dictionary formats. One such format is the one created and popularized by Jesse Antunes of Six Fried Rice. (Let’s call it SFR format.)

````
"<:name:=Calvin:>
<:age:=5:>"
This module provides a means for systems employing SFR format to easily integrate Let-based modules with minimal effort.
````

## Usage

The ParamConverter module provides one script for converting from SFR format to Let Variables and one for converting from Let Variables to SFR format. The most straightforward approach is to create a wrapper script for each Let-based script you’d like to call. This wrapper script will convert the parameters and script results for you. The module includes an example script that shows you how. You can also see it in action in the enhanced demo file for the ErrorHandling module.

To call a Let-based script, just copy the example script from this module and redirect it to the Let-based one.

You also have the option of adding a prefix to your variables. For example, you can set the variable prefix to "__" to have ````"<:name:=Calvin:>```` converted to a variable named ````$__name````.

## Integration

Just import the ParamConverter script folder and begin making wrapper scripts. Remember also to add the initialization script to your launch routine.

## Download and Installation

There should be a "Download ZIP" button on the [GitHub page](https://github.com/DonovanChan/ParamConverter).

To install, just import the ParamConverter script folder from ParamConverter.fmp12 into your solution.

## Contact

Donovan Chandler  
donovan_c@beezwax.net