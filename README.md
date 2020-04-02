# COVID-19
Like most other people, I have gotten interested in the SIR curve modeling for the Coronavirus outbreak. I had a play with the mathematical model, and instead of replicating it again, I thought I would try something different: Agent Based Modeling.
Preface - I am not an epidemiologist, and the basis for my assumptions below are a little arbitrary.

## Agent Based Modeling
With agent based modeling, instead of relying on mathematical principles, idiots like me rely on a simulation of different actors (agents) following simple rules to create basic (or complex) models.
I thought it would be interesting to see if with simple inputs, it would replicate the same curves we see with the differentiation based SIR model.
One of the advantages of Agent Based Modeling is the ability to create fairly complicated models without in depth mathematical knowledge.
### Concept
I created a 100 x 100 hexgrid community that our agents would live in, and initialized 100 agents (with 2 infected) at random points. They moved about at random with 20 hour days - each hour they would move one grid space at random (although not directly backwards (in an attempt to stop everyone from just jittering around in place). Once infected they would be contagious with a radius of 5 for approximately 14 days, before becoming immune.
The agents would follow simple rules that would affect the outcome - washing hands would reduce the area that they were contagious, social distancing would reduce the amount they moved (from 20 grid spaces a day to approximately 6).
I created 4 fairly basic simulations:
1) Uncontrolled - noone washes their hands, and people run around like idiots having parties daily
2) Social Distancing - people stay home, but touch their faces like maniacs
3) Hygiene Changes - people wash their hands but still have parties
4) Social Distancing and Hygiene Changes - everyone stays home and wash their hands
