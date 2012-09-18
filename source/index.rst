.. FLL Programming For Coaches documentation master file, created by
   sphinx-quickstart on Fri Sep 14 21:03:39 2012.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

=====================================
 FLL Programming For Coaches - Notes
=====================================

Contents:

.. contents:: `Table of Contents`
   :depth: 3

.. toctree::
   :maxdepth: 3

Sources
=======

.. note:: 

   * I'm using other coaches fine presentation materials for the most part. 
   * Therefore, most notes simply refer to the slide/presentation I'm working from.
   * So I'll start by listing their fine resources.

References
----------
   
`FLL Basic and Advanced NXT-G Programming for Coaches`_ - By Tony Ayad
    * Posted on the *Los Angeles Region FLL Team Resources Page*
    * Hereafter refered to as `Ayad`_

    This is a newer presentation and one of the best I've found.  I strongly suggest 
    that you review this presentation. Anything you don't already know? Stop 
    and read/study carefully.
    This presentation (the basics part) was used on one of the Coaches conference 
    calls just within the last week or two so go find a playback of that call 
    on the FLL site.

`2011 Cougar Advanced NXT-G Programming Workshop v2.1`_ - By Cougar Robotics
    * Hereafter refered to as `Cougar Presentation`_

    Another excellent and recent presentation.  Look on the web page for a 
    couple of good samples that go with it.  Covers some topics not covered 
    well elsewhere.  For example, good coverage of a simple "logical AND" 
    alternative using a 1 count loop for synchronization.

`NXT Tutorials by Dale Yocum`_ - By Dale Yocum
    * Hereafter refered to as `Dale Yocum Tutorial`_

    An oldie, but a goodie - primarily for beginners. Notable primarily 
    because of the very nice video format and patient pace of the presenter.
    Doesn't cover all the latest techniques.

`Creating and Using your own Blocks with My Blocks`_ - By Dave Parker (nxtprograms.com)
    * Hereafter refered to as `My Blocks Tutorial`_

    Very thorough overview and tips on creating My Blocks! Some good tips on 
    wiring here as well. 

`Team Hassenplug NXT-G Code Snippets Index`_ - By "Team Hassenplug"
    * Hereafter refered to as `Hassenplug Tips`_

    Excellent well documented tips! Also, some really good information on 
    data logging here. Hassenplug and friends are serious adult Lego 
    enthusiasts so some of what is on their site is not appropriate for FLL.
    For example, they use specialized blocks created in Labview in some 
    cases that wouldn't be legal in FLL competitions. 

`FLL Programming 101 with NXT-G`_ - HighTechKids.org
    * Hereafter refered to as `NXT-G 101`_

    Another oldie, but goodie.  However, it is a bit dated and almost all of it 
    is covered in one of the above.  However I may refer to a slide or two 
    and you may want to review...

Specialized Tools and Techniques
    * `nxtRICEditV2`_ - Tool to create custom graphics for the NXT Screen!
    * `Make a custom My Block icon`_ - Describes how to create/use custom 
      graphics for use in My Block icons.


Notes
=====

.. note:: **Important Note**: At the moment these notes are for an **advanced** class 
          so the below notes suggest skipping slides and resources that I assume an attendee 
          at an advanced class should know.  If you are not ready for an advanced class then 
          **don't skip anything**!

Tony Ayad FLL Programming Beginner and Advanced
-----------------------------------------------

Coverage from `Ayad`_

1. Slides 1 through 9, SKIP

#. Slide 10, Mention Profiles  Mention Custom My Block Folders

    * Create a folder called "Peter" at the appropriate spot

#. Slide 12, Mention difference between Motor and Move blocks

#. Slide 16 and 17, Talk about the PID and accumulated error

    * Introduce concept of **reset motor** block and use of **Rotation Sensor** 
      block to "start from 0".

#. Slide 23, brief pause to talk process.

    * Program one distinct action at a time, test, make reusable (if team is 
      knowledgeable about My Blocks, don't force it)

#. Light Sensors - **GO to Black Line** program

    a) Slide 25 through 37.  Will have to skim some, but need to cover...
       
        * Calibration

        * View Sensor Program (download from `Dale Yocum Tutorial`_)

            - Worth pausing to discuss screen output and number to text

        * **Example 1A**: Simple go to black with Loop till sensor

            - Point out problem (how do we tell it the light value?)

        * Cover Light Sensor Block (not covered till slide 47 unfortunately)

            - Note that it takes input (target light value)

        * **Example 1B**: Introduces Light Sensor Block in a Loop

        * **Example 1C**: Adds a constant to feed in the target light value

        * At this point we *could* make a my block

          But let's think first of other things we might want to control
          
              - Option to stop at end or keep going?

              - Option to provide a power level?

              - Do we have to get past a *dark* area first before we start 
                looking?

        * **Example 1D**: Has these additions

          .. note:: Note how we've already set up constants to provide 
                    these values!

Coverage from My Blocks Tutorial
--------------------------------

1. My Block Time!

   `My Blocks Tutorial`_ covers this very nicely!
   
   * **Example 1_D-MB**: Demonstrate creating a my block from 1D.  Can view finished example.

   * Input naming

   * Save location

   * Try Using 1_D-MB in a program
 
#. My Block Output!

   * **Examle 1_E**: Same at 1_D, but it is printing out the distance travelled.
   
       - Demonstrate making a my block out of 1_E

   * **Example 1_E-MB**: Shows the completed My Block.  **Example 1_F-MB** 
     shows adding sound effects, just for fun!

   * **Exmaple 1_F_USE**: Demonstrates use of the program.

       - Show a program that goes over two lines with just this block.

#. **Example 3**: Follow line till Ultrasonic.  Nothing new really,...


Tasking with AND, OR, etc
-------------------------

In programing a logical AND means we two things need to be true for the "whole" 
thing to be true.

A logical OR means one or the other thing needs to be true for the "whole thing" 
to be true.

Here we are talking about a similar concept, but with tasks.

1. AND

   Means I want my program to wait until two distinct things are done before 
   continuing with the rest of the program.

   * We've seen one already with the register to wall

   * Other options?

   Can be done with complex conditions, but a neat trick is to use a 1 count loop!

#. OR

   A good example can be found in the `NXT-G 101`_ presentation on 
   **slide 81**.

   * AND can also be done in a similar way, but the task synchronization trick 
     is usually simpler.

Putting it all together
-----------------------

A quick look at a complex program that uses multiple my blocks.

More Tips and Tricks (and things I didn't have time to cover!)
--------------------------------------------------------------

1. The `Hassenplug Tips`_ page is an **excelent** resource, review it!

#. Wiring into a switch block

   * Generally wiring is a pain!  The `My Blocks Tutorial`_ covers that, review it and practice!

     All the more reason to use **My Blocks**!

#. Debugging Tips (there are many)

   * Sound

   * Stop for 1 second

   * Video tape robot and play back in slow motion!

   * Data Logging (more in a moment)

   * Print stuff to screen

#. Tricky to move things between computers

   * Try the "pack and go" feature in 2.0

#. Organize blocks by making custom myblock folders

#. Really crazy stuff!

   * Make your own ".ric" files which can be displayed on the NXT screen.

     Our team did that "way back when" to display a large number on the NXT 
     screen for what program we were on.

   * Make ".png" files which can then be put in a special folder and used for 
     custom My Block pictures.


.. _`Ayad`:
.. _`FLL Basic and Advanced NXT-G Programming for Coaches`: http://fll.larobotics.org/Resources.html
.. _`Cougar Presentation`:
.. _`2011 Cougar Advanced NXT-G Programming Workshop v2.1`: http://www.cougarrobot.com/index.php?option=com_content&view=category&layout=blog&id=78&Itemid=118
.. _`Dale Yocum Tutorial`:
.. _`NXT Tutorials by Dale Yocum`: http://stemcentric.com/nxt-tutorial/
.. _`My Blocks Tutorial`:
.. _`Creating and Using your own Blocks with My Blocks`: http://www.nxtprograms.com/help/MyBlocks/tutorial.html
.. _`Hassenplug Tips`:
.. _`Team Hassenplug NXT-G Code Snippets Index`: http://www.teamhassenplug.org/NXT/NXT-GCodeIndex.html
.. _`NXT-G 101`:
.. _`FLL Programming 101 with NXT-G`: http://www.hightechkids.org/for-teams/coaches-library
.. _`nxtRICEditV2`:
.. _`nxtRICEditV2 - Tool for creation or modification of RIC files for the Mindstorms NXT`: http://ric.dreier-privat.de/Docu/index_eng.htm
.. _`Make a custom My Block icon`: http://thenxtstep.blogspot.com/2010/07/custom-nxt-g-myblocks.html


Indices and tables
==================

* :ref:`genindex`
* :ref:`search`

