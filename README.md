9 Rules of Debugging - Notes

    By David J Agans

How can it work so easily?

   • Whenever it takes a long time to find a bug it is typically because one has neglected some essential or fundamental rule.
   • Once the rule was applied, the bug was quickly found.
   • Understanding and applying these rules makes a big difference to debugging quickly.

   
  Debugging vs Troubleshooting

    • Debugging usually means a design does not work out as planned.
    • Troubleshooting means to figure out whats broken in a particular copy of a product, after knowing the design is good.


  Debugging Rules
  
    • Understand the system
    • Make it Fail
    • Quit Thinking and Look
    • Divide and conquer
    • Change one thing at a time
    • Keep an audit trail
    • Check the plug
    • Get a fresh view
    • If you didn't fix it, It aint fixed.



  Understand The System

      • Reading the manual is always the first step to solving something.
      • You cannot debug a system that you do not understand in the first place.
      • In a codebase this includes reviewing the comments and intention of the system design.
      • Though one should be cautious of the original engineers being wrong, however understanding their vision can be helpful.

    Know your tools

      • Your debugger tools are your eyes and ears into the system.
      • Take the time to learn everything about your tools.
      • The key to see whats going on is often correlated with how well your debuggers and analysers are set up.

    Dont guess, look it up

      •  There is always detailed information somewhere by the creator of what your interacting with.
      •  Sometimes it is possible to be debugging while looking at the wrong stuff,


    Chapter Summary

    •  Read the Manual.
    •  Read everything in depth.
    •  Know your fundamentals.
    •  Know the roadmap.
    •  Understand your tools.
    •  Look up the details.
    


  Make It Fail

  • Reproducing failure can help you hone in on the bug.
  • Knowing exactly what conditions it fails within, will help fix the bug.


Chapter Summary

    •  Do it again.
    •  Start at the beginning.
    •  Stimulate the failure.
    •  Find the uncontrolled condition that makes it intermittent.
    •  Record everything on the find signature of intermittent bugs.
    •  Dont trust statistics too much.
    •  Know "that" can happen.
         Basically the most random and unprobable cause could give you hints as to how to fix the problem.
    •  Never throw away a debugging tool as it can be used in the future.

    
    
   Quit Thinking and Look

    •  Guesswork is often wrong even if you are experienced.
    •  Though the author mentions that guessing is still valuable, especially if you understand the system. However, you should guess only to focus the search.
    •  Keep looking until the failure you can see has a limited number of possible causes to examine.

    Chapter Summary

    •  See the failure.
    •  See the details.
    •  Build instrumentation in.
    •  Add instrumentation on.
    •  Dont be afraid to dive in.
    •  Beware of Heisenberg (Dont let instruments overwhelm your system) (Not Walter White).
    •  Guess only to focus your search.

    
Divide and Conquer

    •  Agans mentions a technician who is debugging a terminal and correctly implements the other methods of debugging but highlights the strategy or divide and conquer to rule "bad halves" out
    •  He also mentions successive approximation which is explained as starting at one end of the range and then going halfway to the other end to see if you're past or not. Continued by going 3/4ths ect...
    •  When applying this you should try to start at the bad end and work your way up
    •  Its hard for a bug to keep hiding when its hiding place keeps getting cut in half

    Chapter Summary

    •  Narrow the search with successive approximattion (Guess from 0-100 in 7 guesses)
    •  Get the range ( If the number = 135, then guess 100 then widen it)
    •  Determine which side of the bug you are on (Try to be in the bad)
    •  Use easy to spot test patterns ( Start with clear water and make it obvious when goo enters)
    •  Start with the bad (Start broken and work your way up)
    •  Fix the bugs you know about (They can interact with eachother creating a mess)
    •  Fix the noise first ( Watch for things that will screw up the rest of the system)

    
Change one thing at a time

    •  Agans mentions that sometimes you need to take a step back and observe, he references the brass bar in nuclear plants. If something urgent happens employees are trained to first hold on to the bar and             observe. It is better to do nothing sometimes than mess it up more.
    •  Another strategy he mentions is comparing to a good one, he mentions 2 debug logs side by side. 1 with the bug and 1 thats in good condition. Going though these although boring can be effective.
    •  If you replace 4 parts on a board to fix your problem. Great you fixed it, but you now have no idea what was broken. So just replace one thing at a time and keep in mind
       of what changed since it last worked.
    •  Its hard for a bug to keep hiding when its hiding place keeps getting cut in half
    
Chapter Summary

    •  Isolate key factors (Dont change the watering schedule if you're looking for the effect of the sunlight
    •  Grab the brass bar with both hands (If you try to fix a nuke without knowing whats wrong, you can make it worse)
    •  Change one test at a time 
    •  Compare the result with a good one.
    •  Deternube what changed since it last worked.
    
