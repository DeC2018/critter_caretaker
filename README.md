# critter_caretaker

The Critter class is the blueprint for the object that represents the player’s
critter. The class isn’t complicated, and most of it should look familiar, but it’s
long enough that it makes sense to attack it in pieces.
After some initial comments and statements, I begin the Critter class.
m_Hunger is a private data member that represents the critter’s hunger level while
m_Boredom is a private data member that represents its boredom level. I’ll go
through each member function in its own section.
The constructor takes two arguments, hunger and boredom. The arguments each
have a default value of zero, which I specified in the constructor prototype back
in the class definition. I use hunger to initialize m_Hunger and boredom to initialize
m_Boredom.
Next, I define GetMood().
The return value of this inlined member function represents a critter’s mood. As
the sum of a critter’s hunger and boredom levels, a critter’s mood gets worse as
the number increases. I made this member function private because it should
only be invoked by another member function of the class. I made it constant
since it won’t result in any changes to data members.
PassTime() is a private member function that increases a critter’s hunger and
boredom levels. It’s invoked at the end of each member function where the
critter does something (eats, plays, or talks) to simulate the passage of time. I
made this member function private because it should only be invoked by
another member function of the class.
You can pass the member function the amount of time that has passed;
otherwise, time gets the default argument value of 1, which I specify in the
member function prototype in the Critter class definition.
