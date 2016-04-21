#PD Tools and Projects

# 2016 Update
It has been well over two years since I worked on any PureData projects. 
I'm refreshing the repository and plan on updating it regularly.

# Road Map
Goals included in this repository are as follows:

* Create a standard library of generic PureData tools to have as an include path
* Have controller-specific folders and programs within those folders
* Remove old scripts that are unnecessary, refresh old ones with new code
* Create a generic-as-possible project that can be used with Vanila PD (no Gem/extended)
* Include screenshots of each program belonging to a controller in each folder readme.

#PD Tools/Projects

Pure Data is a visual audio-programming language designed
at creating interactive applications. It works a lot like
Max/MSP by Cycling '74, and was made by the same guy who did
make Max.

#Why Can't I Read this Garbage?

It's a *visual* language, meaning it can only be *viewed*.
You need the PureData application set to view PD scripts 
properly.

I'm working on trying to upload screenshots of notable programs to make it easier.

#Where do I get PD?

Get it [here](http://puredata.info/)

#Contributing / Issues

If you'd like to submit fixes or report issues, please do.

# Program Design

To keep in synergy with PureData semantics:

* Any object that outputs an audio signal should end in "~"
* Otherwise, it should be named normally [a-zA-Z0-9|(\_,!)]

Example: if you have an object that sends out a cosine wave, name it "cos~".

This is designed so that the user knows what the object will output, without 
having go inspect it.

If you are using SENDs and RECEIVEs (*s* and *r*), be sure to prefix variables with "$0-" to make them 
unique to the program instance. Otherwise they will cause overlap with other 
instances of programs (if you have two synths sending out a mix signal, 
another instance can override the send).

If code is starting to look mangled, consider grouping code inside of objects 
to organize objects better.
