## Sound to Keyframes

There are many [tutorials on the
internet](https://www.youtube.com/watch?v=G3Yfkh9b2_8) on how to "bake sound to
f-curves", "sound to keyframes", "bake sound to effects". Here is a very quick
run-down on how to test/start with this with BlenderDMX addon:


1. Create a basic scene:
    - Add single fixture
    - Add haze for volumetric beams
    - Clear the fixture and set intensity and color

    ![image](../media/sound_baking_00.jpg)

2. Save this a keyframe:
    - Press Add Keyframe in DMX - Keyframe recorder
    - Open the Timeline
    - In the Timeline, uncheck the "Show only selected"

    ![image](../media/sound_baking_01.jpg)

3. Bake sound to F-curves:
    - Open Graph editor
    - Select desired item in the listing of recorded elements, for example Spot size (Zoom)
    - Select Channel - Sound to Samples
    - This adds the audio waveform to the timeline
    - Now when you play the timeline, the zoom

    ![image](../media/sound_baking_02.jpg)

    ![image](../media/sound_baking_03.jpg)

4. Optional - Add sound to the Video sequencer
    - Open Video Sequencer
    - Select Add - Sound and select the same audio track as before

    ![image](../media/sound_baking_04.jpg)

5. Done, play the animation with sound:
    - Note: audio seems a bit offset from video while playing in the web browser.

    {{< video "../media/sound_baking_05.jpg" "../media/sound_baking_05.mp4" >}}
