# DOTS-Dynamic-Bone-Demo
A Demo Version of the unfinished DOTS Dynamic Bone System 

This is a demo version of the DOTS Dynamic Bones system.

If you want to access the full version check out these links:

Documentation: https://steven9smith.github.io/DOTS-Dynamic-Bone/

Asset Store Page: https://assetstore.unity.com/packages/tools/physics/dots-dynamic-bone-204257

## Quick Demo Documentation

In this demo you have acess to two Components: the DOTSDyanmicBoneComponent and DOTSDynamicBonesComponent...ignore the DOTSDynbamicBoneComponent because the DOTSDynamicBonesComponentUses it anyway.

I will now break down each option and how to use it but please look at this image first to know what works and what doesn't work.
Red means it has been disabled and the blue means "I'm pretty sure it does nothing" or "not implemented". 

![image](https://user-images.githubusercontent.com/26945893/134696931-78f3ae4b-665a-42cb-8481-bd7215eabaa4.png)

### Rig Component
  - This is the GameObject that contains the RigComponent

![image](https://user-images.githubusercontent.com/26945893/134694892-e45c7b85-48b5-4684-85be-64f3dcc56537.png)

### Bones
  - This is a list of DOTSDynamicBoneComponent. this allows you to have many diffent sets of dynamic bones on a single entity.
![image](https://user-images.githubusercontent.com/26945893/134699813-248221d6-36d8-44bd-a67a-fcfdbc6028b3.png)

### Update LocalToWorld Transform
  - due to the way ECS and it's internal systems work I didn't need to modify the LocalToPrent,LocalToWorld,Translation or Rotation values of an entity. However, of you want the calculated to positions to be reflected onto the entity itself then set this to true. 
  - NOTE: the LocalToWorld Positions ARE NOT calculated, all I do is set the LocalToRoot results to the entity's LocalToWorld...I'll change this later/add more options.
![image](https://user-images.githubusercontent.com/26945893/134699681-b3454adf-efaa-4da8-9c7b-1a313536a574.png)

### Use AnimatedLocalToRoot
 -  always leave this true otherwise....stuff breaks. 
 -  What does this do? This performs a super secret mathmatical formula that I don't feel like converting into a proper mathmatical formula.
![image](https://user-images.githubusercontent.com/26945893/134699644-3d1dda5a-bb2d-4a6a-a5dd-4a3679ee609e.png)

The rest of the components parts have tooltips that tell you what they do.

Please Give Your Feedback at this Unity Forum Link :)
https://forum.unity.com/threads/dots-dynamic-bones-wip-demo-v0-8-2.1176287/

#FAQ

Why is this a demo? 
- because it's not done.

the root bone keeps jittering, is this normal?
- yes, it has to do with a physics calculation. In order to reduce the jittering please set the inert value > 0

Why are there components that do nothing?
- cause i'm not done


