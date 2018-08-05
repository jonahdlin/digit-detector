# Digit Detector

In this project I'm hoping to gain and refine some C++, OOP and calculus skills by creating a neural network to recognize handwritten digits. I'll be writing all the code from scratch without looking at any code examples, guides or tutorials, apart from [this 3Blue1Brown series](https://www.youtube.com/playlist?list=PLLMP7TazTxHrgVk7w1EKpLBIDoC50QrPS).

I've never attempted a project like this and at this point it's been 3 months since I last used C++, so let's hope I can make something cool happen.

## Why?

Why not? I'm looking to cement some C++ skills, since I found it super interesting when I took a course in it at Waterloo. After watching that 3Blue1Brown series (2 or 3 times), I thought I could use some OOP, C++ and calculus together to make something neat. So here we go.

## Roadmap
### Milestone 1 - Structure

The biggest test of my OOP and C++ skills. I want to set up a modular and adaptable neural network framework that will make it easy to complete this project, but also be expandable to others. For the purposes of this project, this milestone will include:

- A neural network class that produces a neural network with an input layer, followed by *n* hidden layers, followed by an ouput layer, all of variable size
  - Has methods for simply producing output for a given input
  - Has methods for tweaking the weights and biases of its edges
- A trainer class that consumes a neural network and a set of training data and mutates the neural network to work properly
  - This is a big responsibility, so I may end up changing the structure as I go along
  - No complex functions or behaviour will be set up at this stage, just the structure with some dummy methods
- A class that can take a 16x16 pixel image and translate it into an array of grayscale pixel activations between 0 and 1
- A `main.cc` that combines all these parts into a workflow where a neural net is created, (fake) trained, and then used with an image

After I'm done here, running the program should produce some garbage output number between 0 and 9 as a "guess" for the input, though this will be completely random as all the weights and biases will be garbage values.

### Milestone 2 - Training

The biggest test of my math and calculus skills. In this one I'm going to implement the training functions in the trainer class so the thing actually makes real guesses at the end that will ideally be correct 95% of the time or so. This'll be the true test of my mathematical might and whether or not I actually understood that video series I mentioned.

### Future Milestones

> Be forewarned, all the stuff past milestone 2 is a real pipe dream. If I can get an actual neural net going, I'll be incredibly astonished. If that works, then I could continue with this stuff.

My real end goal with this project is to combine it with web technologies (which I am already well-versed in) to create a nice frontend to use this with. Since it's boring to just input values and have the machine guess them, I'm hoping to make it a bit more interactive. I will store snapshots of the neural network at different times in its training, and allow the user to travel backward and forward through time and see how well the neural net works. I could also show what the activations in the hidden layers do interactively, in a similar way to the 3Blue1Brown video series.

Doing this will first of all involve me figuring out some way to hook up the C++ code I will have written to some form of backend and primitive database. Then I'll need to write some API for getting the snapshots, activation composites, etc., as well as for receiving and returning output for a json of image pixel activations (since I'm not gonna be sending the whole image back). Lots of ifs and maybes here. After all that, I can get to the frontend stuff, which should be the only straghtforward part of this whole thing.

