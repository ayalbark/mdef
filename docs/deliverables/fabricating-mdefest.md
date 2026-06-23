# Fabricating MDEFEST

## ECHO V1 - Training Human Echolocation

![Echo](../images/echo%201.png)

## [Link to Hackster.io project](https://www.hackster.io/ayal/echo-v1-912686)

<iframe frameborder="0" height="385" scrolling="no" src="https://www.hackster.io/ayal/echo-v1-912686/embed" width="350"></iframe>

ECHO V1 is a wearable training device for human echolocation. It asks whether technology can open up a new perceptual reality without becoming the thing we rely on forever. Instead of building an assistive device that replaces a human capacity, I wanted to build something closer to training wheels: a device that helps the body learn, and eventually becomes unnecessary.

The device is worn around the head. When the user makes a mouth click, a microphone detects the sound and triggers three ultrasonic sensors facing left, center, and right. Those sensors read the distance of nearby objects, and five haptic motors around the head translate that spatial information into vibration. The closer the object, the stronger the buzz. Over time, the idea is that the user begins to associate the echo they hear with the haptic feedback they feel, until the haptic layer can be reduced or removed.

## Where It Came From

This project did not appear suddenly during Fabricating MDEFEST. It grew out of the three previous Cognitive Orgies projects I worked on this year. Each one helped me understand a different part of the same question: can the body learn to perceive through an artificial sensory scaffold?

In [Cognitive Orgies I](cognitive-orgies-i.md), Compborg: Second Spine explored how environmental information could become bodily sensation. The project translated compost moisture data into haptic patterns along a wearable spine. It was speculative, but the key discovery was practical: vibration can become meaningful if it is mapped clearly enough and repeated enough. The body starts to read sensation as information.

In [Cognitive Orgies II](cognitive-orgies-ii.md), StockSense moved that logic into a live data system. We built a wearable that translated stock market information into haptic feedback on the chest. The project worked, but it exposed a problem: a first-time wearer mostly experiences unfamiliar vibration as noise. Sensation is immediate, but perception has to be trained. That gap became much more interesting to me than the data itself.

In [Cognitive Orgies III](cognitive-orgies-iii.md), OuterBody moved away from data translation and focused on embodied experience. We used phones, video streaming, and a VR headset to choreograph a temporary out-of-body experience. The important lesson was that the technology alone was not enough. The performance, staging, and instructions were what allowed people to feel displaced from their own body. This helped me understand that ECHO could not just be a device that speculates an alternative future, it needed to be a device that lets the user experience one.

ECHO brings those three threads together. From Compborg, it takes haptic information as a bodily language. From StockSense, it takes the problem of training sensation into perception. From OuterBody, it takes the importance of first-person experience and choreography.

## Fabrication Process

The fabrication process took around six weeks. I started before the Fabricating MDEFEST course officially began, which gave me time to make a small prototype and start the course with clarity.

My first prototype used audio feedback. The sensors detected objects and returned sound to the user. It worked in the sense that the user could understand direction and distance, but it failed conceptually. If the device used sound to communicate the answer, then the user could not hear their own echoes clearly. That meant there was no chance for the brain to couple the actual echo with the feedback. It was helping too much, in the wrong way.

So I pivoted to haptics. This made sense because I had already spent the year working with haptic motors in Compborg and StockSense. The new challenge was how to place the sensors, motors, microphone, Pico W, and power supply on the body in a way that could survive people actually using it.

Shyam suggested using a medical face shield as the structure. That solved a lot of problems at once: it was adjustable, light, strong enough to hold components, and already designed to sit on a head. I burned holes into the plastic for the ultrasonic sensors, mounted the microphone with bent copper wire, glued the motors to the headband, and eventually soldered everything onto a flexible matrix board.

The cable management took far longer than I expected. It was tedious, but it also made the project feel like it crossed from prototype into artifact. 

## When AI Could Not Direct Me

One of the most rewarding parts of this project was how badly AI failed to help with the integrated design. I tried to have it generate schematics for the circuit and wiring layout, but it could not produce anything I could actually use. Usually, I am happy to use AI as a guide when I am working through technical domains I do not fully understand. But in this case, it kept pointing me in unusable directions.

At first this was frustrating. In hindsight, it was a blessing in disguise. Because AI could not direct me, I had to slow down and draw the wiring by hand. I had to understand what each row, column, pin, motor, sensor, and connection was doing. I ended up labeling the flexible matrix and thinking through the circuit spatially. That made troubleshooting much less mysterious. When something broke, I was not just asking a chatbot what to do. I had enough of a mental model to diagnose it myself.

This changed my relationship to the project. Instead of assembling a thing from instructions, I felt like I was learning the logic of the device from the inside.

## Murphy's Law: The Mic Breaking

Murphy's Law states that anything that can go wrong, will go wrong. I had my own invocation of Murphy's Law the day before the event. Up until then everything worked perfectly, then  the microphone suddenly stopped working. I tried to diagnose it from every angle, but the conclusion was annoyingly simple: the mic had broken.

This was stressful, since there were no more mics available to use in the Fab Lab. Luckily, I remembered that Dani had given me a spare microphone earlier in the process, so I went back to the Fab Lab and soldered it in. The fix worked, and the project survived. The takeaway:  ALWAYS grab backup components. 

Like the AI failure, the broken mic interrupted the smooth fantasy of fabrication. But both interruptions made the final device stronger because they forced me to understand more of it directly.

## Performing ECHO at MDEFEST

For MDEFEST, I did not want people to just look at ECHO on a table. The project only makes sense when someone wears it, loses visual certainty, and has to negotiate space through sound, vibration, and another person's presence.

I set up a partner activity. One person wore the device and was blindfolded. Their partner held a movable wall, which was also a poster explaining the project. Before each round, I drew a route on the ground with chalk. The partner with the poster-wall had to direct the blindfolded participant along the route using the poster-wall to create an echo target to guide them through the space.

This setup was not a pure echolocation test. It was a structured training scenario. The movable wall made the environment legible enough for a first encounter with the device. The partner made the activity social and performative instead of purely technical. The chalk route gave the audience something to understand from the outside, while the person wearing the device experienced the uncertainty from the inside.

In that sense, the performance borrowed a lot from OuterBody. The technology mattered, but the choreography mattered just as much. Without the blindfold, partner, chalk route, and wall, ECHO would have been a boring demo. With them, it became an embodied encounter.

## How It Was Received

The reception at MDEFEST was encouraging because people understood the project quickly once they saw someone using it. The device looked strange enough to invite curiosity, but the activity gave people a clear way in. They could watch someone move through space differently, and then imagine what it might feel like to try it themselves.

The partner format also helped. It made the experience less intimidating. The blindfolded person was vulnerable, but not alone. The person holding the wall became part guide, part obstacle, part collaborator. That dynamic shifted the project away from a heroic solo technology narrative and toward a training relationship.

Different people responded with different levels of comfort. Some trusted the device and partner quickly. Others moved slowly and hesitated. That difference was useful. It showed that ECHO is not only about whether the hardware works. It is about how quickly people can form trust in a new sensory loop.

## Limitations

ECHO V1 worked as a navigation tool in a structured setting. People could use it to follow a moving wall and understand something about nearby space. But that does not prove that they learned echolocation.

This distinction is important. Following haptic feedback is not the same thing as developing a durable perceptual skill. The real question is whether repeated practice with the device can produce improvement after the device is removed. If it cannot do that, then ECHO is an assistive navigation device. If it can, then it becomes a training device.

That is the difference I want to investigate next.

## Next Steps

Next year, I want to turn ECHO from a working prototype into a structured training study. The most important next step is testing whether the device can actually produce device-independent improvement in echolocation.

The future experiment would involve several weeks of daily practice, probably around 20 minutes per day. Participants would train with ECHO, then complete obstacle detection and distance estimation tasks with and without the device. A retention test after a gap would be especially important, because that would show whether the learning stayed in the body.

I also want to document the phenomenological side of the training. The moment I am most interested in is when a participant stops saying "I hear something" and starts saying "something is there." That shift from interpreted signal to perceived space is the real design goal.

There are also hardware directions to explore. Camera-based depth sensing could give richer spatial information than ultrasonic sensors, but it would also create a harder translation problem. Stereo microphones might be more faithful to actual echolocation, because they could amplify or analyze the returning echo itself instead of substituting sensor data for it. Before moving too far in that direction, though, I want to understand what this first version can teach.

For now, ECHO V1 feels like a synthesis of the year: a wearable, a performance, a speculative question, and a technical prototype all folded into one project. It is still rough, but it points toward something I want to keep working on: technology that expands human capcity without reliance.
