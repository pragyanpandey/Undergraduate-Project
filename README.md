# Undergraduate-Project
1 Start by taking videos of people moving around. Detect humans in the first frame using pretrained ML codes which are widely available.

2 Now follow each human using a so called kernel tracker, link mean shift/camshift that used the general colour information to follow the individual.

3 Monitor states of each individual (bearing state) and classify as frontal, left profile, right profile, rear and their combinations.

4 People can get temporarily hidden behind other people/objects. So classify 'visibility state'  as fully visible, partially visible, invisible when the person is located well within (10% of the width/height of frame away from the boundary) the frame boundaries.

5 A person can be in various poses: standing, sitting, lying, others. Ckassify the 'pose state'.

7 'camera proximity' state. On a scale from too far, far, medium, near, too near, which helps in deciding if the person is fit for doing face recognition on, with some confidence.

6. 'motion state'. position, velocity acceleration (all numerical vector quantities).

All the above states can vary from frame to frame. So each of the state classes has a value for each frame. You may use ML approaches by training with examples to do all these classifications except for the motion state, which can simply be directly measured in pixels.

All states should be logged for each individual against timestamp.
