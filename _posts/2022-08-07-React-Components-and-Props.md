---
published: true
---
## What Are Components?
Lets take a look at Youtube as an example. If you take a look at the screen when you are watching a video, you'll see that the display, or App, can be divided into sections that display different data in similar formats: 
App
- Left: Main Video 
- Right: Suggested Video
- Bottom: Comments

![Overview Highlighting Components](https://user-images.githubusercontent.com/52802563/183313985-cdc85c63-b41f-460a-a4da-2a485e57f56f.PNG)

Lets break down each of these sections so we can have a deeper understanding of components.

### Left: Main Video

<img src="https://user-images.githubusercontent.com/52802563/183315127-331c62bb-c809-4c21-a45f-6577a8793862.PNG" width="500">

When we look at the left side of the screen, you will see the video itself. Overlayed on the video, there are buttons to pause, play, control the volume, skip forward on the video, enable closed caption and more. Just beneath the video, you can see the video title and buttons to like, dislike, share, download, clip and save. 
You'll notice how some of those button icons are familiar and are displayed at other parts of Youtube's site.

![Buttons](https://user-images.githubusercontent.com/52802563/183314960-6d1aab29-d81f-41df-9bd1-ea0b4994f130.PNG)

### Right: Suggested Video

<img src="https://user-images.githubusercontent.com/52802563/183315105-e3e1d264-9b9c-4362-b9d5-769663adc097.PNG" width="400">

If you take a look at the right hand side of the screen, you'll see the suggested video pane. You can keep scrolling down and more videos will populate. This component can be treated as a list. You'll also notice that within this component, you can see there is an iteration of a same type of component in the form of a card. There is a screenshot of the video, the video title, the Youtuber username, how many views, and when it was published. A way to handle this list is to iterate in a for loop where it iterates through the information and only calls on the card. You also know that the Right Coponent interacts with the Left by when selecting a suggested video, it becomes the one that is displayed on the Left Main Video Component.


### Bottom: Comments

<img src="https://user-images.githubusercontent.com/52802563/183314567-34b5ac7f-317d-42a0-9a40-1ecb59a7cc48.PNG" width="500">
