# Flipbook

A full-stack animation webapp made with Typescript, React, MongoDB, in collaboration with aong9, oanders6,dsaunde2,bmaizes.

## Background
Making animations has an accessibility problem. To make quality animations this requires professional software which is often bricked by a steep learning curve, expensive paywalls, and hardware demands. We gathered knowledge about this problem through interviews with peer animators, non-animators with interest in doing so, and through reviews of other animation software.

Our project solves this by bridging the accessibility gap in animation with a simple sketch and tracing based interface. Of course, a non-software based solution would be to produce physical flipbooks to be drawn on, but our software allows the fast creation of animation cells and tracing of existing images/video frames. Doing this on a physical flipbook would require a large of paper resources and a backlit tracing surface. 

This app should be a seamless, easy to access application for any users. It should be quickly deployable and with little barrier. The idea is that users will use it whenever they seek to animate something or want to work on an animation project or as a reference to other development projects. 

## Structure

Whiteboard data module (model) → stores the data from user input to the website, ex. a series of drawn frames, by calling on the animation module via API

Whiteboard visual module (view) → visually displays the data from the whiteboard data by calling on the animation module via API. This model will be made accessible through ARIA labels and descriptions, and with keyboard shortcuts like enter = move to the next frame, shift + enter = go to previous frame, shift+tab = hide/show the outline from the previous frame

Animation module (controller) → stores data from all the frames, putting the relevant frame onto the screen when appropriate and allowing new data to be added. Communicates with both the whiteboard visual and whiteboard data modules.

Export module (model) → converts the data for a selected animations into either a GIF or mp4 based on the user’s choice. 
