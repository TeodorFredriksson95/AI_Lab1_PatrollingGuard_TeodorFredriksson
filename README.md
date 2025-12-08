# A Lab Assignment 01
## Overview
The purpose of this README is primarily to document my progress related to the assignment **"A Simple FSM**, including my answers to the given checkpoint questions which are part of the assignment.

## Research ##
1. In your own words, what is a state in game AI? Give two examples.
- 
3. What triggers a transition between states? Give two examples.
- 
4. Why do you think game AI often uses simple techniques (FSMs) instead of “real AI”
like deep learning?
- 

## Q&A
**Q: What coordinate axes respond to “forward” and “up” in Unity?**

**A:** 
- "up" relates to the Y-coordinate in 3D world space. It's considered a shorthand for *Vector3(0, 1, 0)*. In 2D space, "up" still relates to the Y-coordinate, but is considered shorthand for *Vector2(0,1)*.
- "forward" relates the Z-coordinate in 3D world space. It's considered a shorthand for *Vector3(0, 0, 1)*.

**Q:What happens if the Guard has a NavMeshAgent but there is no baked NavMesh?**

**A:**
- A warning is thrown, indicating that the agent failed during creation. This can happen if the object which the NavAgent is attached too is too far away from or otherwise can't find an available NavMesh. In the above scenario, since no NavMesh has been baked, there is no available NavMesh data so the agent wont be able to find a suitable NavMesh to latch on to.

**Q: In your own words, what is the difference between a path and the movement along that path?**
- I would define a path as the definition of a starting point and an endpoint, with a sequential distance between the two points determined by the A* algorithm, selecting the closes intersectional points of the connected polygons. I would define movement along that path as the objects positional update from the starting position towards the end point, determined by that calculated path, until the end points has been reached.

**Q: Why do we check !_agent.pathfinding before reading remainingDistance?**

**A:**
- An accurate representation of the remainingDistance relies on the agent having properly processed the path, and thus, we want to return if the agent is still processing the path in order to not receive undefined behaviour.

**Q: What happens if we forget to use % waypoints.Length when incrementing the index?**

**A:**
- We will eventually try to access the array with an out of range index, and an error will be thrown.



