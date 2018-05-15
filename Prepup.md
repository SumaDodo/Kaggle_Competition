Introduction -

Large Hadron Collider (LHC) located at CERN headquarters is a large machine that splits particles into smaller and smaller components to 
identify elementary particles from which all matter and energy is derived. It propels sub-atomic particles called hadrons at high speed. 
This particle accelarator is also called as "Atom Smasher" in layman terms.

For more details, refer the [video](https://www.youtube.com/watch?v=FLrEghnKncA) on Large Hadron Collider Simulation.

**Notes:**  
1. The present algorithms are inherently serial, rely on linear dynamics models and scale poorly with detector occupany<sup>1</sup>
Questions:  
- What is the meaning of relying on linear dynamic models?
- What is the meaning of scaling poorly with detector occupancy?

2. Why neural networks?
Ans - Neural networks are known to be very good at finding patterns and modelling non linear dependencies in data<sup>1</sup>

In point based models we use continuously distributed spacepoint measurements and structure them in a list or a tree for learning how to group them as track candidates<sup>1</sup>

**References:**  
1. Particle track reconstruction with deep learning. Steven Farrell et al.
