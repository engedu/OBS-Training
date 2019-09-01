# OBS Sources

## Audio Input/Output Capture

อินพุตนี้ช่วยให้คุณสามารถเพิ่มสัญญาณเสียงหรือเข้าหรือออก (เช่นไมโครโฟนหรือชุดหูฟัง) ไปยังฉาก (scence) ที่ต้องการ 
ไม่ว่าจะเชื่อมต่ออินพุตจากแหล่งมีเสียงเพียงอย่างเดียว หรือมีทั้งภาพและเสียงก็ตาม OBS จะแยกสัญญาณเสียงออกมาและแสดงใน Mixer control
การระบุแหล่งอินพุตแลลสัญญาณเสียง จะช่วยให้เราสามารถเลือกใช้งานเสียงเฉพาะในฉากที่ต้องการ

### คำเตือน:

การใช้งานแหล่งอินพุตนี้ อาจจะทำให้เกิดเสียงก้องหรือสัญญาณหวีดได้ เช่นเดียวกับการใช้เครื่องเสียงกลางแจ้ง โดยเฉพาะหากคีอุปกรณ์เดียวกันที่เลือกไว้ในการ Settings -> Audio ดังนั้น ถ้าหากวางแผนที่จะเพิ่มอุปกรณ์เสียงลงในฉากใดๆ โดยตรง ให้ทำการตรวจสอบให้แน่ใจว่าอินพุตเสียงถูกปิดการใช้งานที่อื่นๆ เสียก่อน


## Blackmagic Device
อุปกรณ์ Blackmagic คืออุปกรณ์สำหรับ Capture สัญญาณวิดีโอลงคอมพิวเตอร์ โดยทั่วไปจะ รองรับช่องสัญาณ Input  ทั้ง SDI และ HDMI ใช้งานได้ทั้งระบบ SD และ HD เหมาะสำหรับงาน Ingest เพื่อตัดต่อวิดีโอ หรือนำสัญญาณจากกล้องเข้าคอมพิวเตอร์เพื่อไปทำ Streaming

Blackmagic ใช้ได้กับโปรมแกรมหลากหลาย เช่น Wirecast , DaVinci Resole , Fusion , Final Cut Pro X , Premiere Pro , Avid , After Effects , Photoshop

![ตัวอย่างอุปกรณ์ Blackmagic](./images/blackmagic-ultrastudio-mini-recorder.jpg)

[รายละเอียดตัวอย่างอุปกรณ์ Blackmagic](https://www.airbondstore.com/th/converter/297-blackmagic-ultrastudio-mini-recorder)

### ตัวเลือกอุปกรณ์สำหรับอุปกรณ์ Blackmage  

รายการ | รายละเอียด
--|--
Device | รายการดรอปดาวน์ที่ให้เลือกอุปกรณ์ Blackmage ที่ต้องการใช้
Mode | ตั้งค่าโหมดวิดีโอของอุปกรณ์ ควรตั้งค่่าให้ตรงกับความละเอียดของเอาต์พุต (เช่นกล้องหรือคอนโซลเกม) สื่อของคุณและเฟรม
Format| เลือกรูปแบบวิดีโอที่อุปกรณ์ใช้งานซึ่งควรตรงกับผลลัพธ์ของสื่อที่ต้องการบันทึก
Use Buffering (Checkbox) | เปิดใช้งานหรือปิดการใช้งานการบัฟเฟอร์ภาพและเสียงสำหรับอุปกรณ์ Blackmagic สิ่งนี้สามารถช่วยแก้ไขปัญหาเกี่ยวกับระบบที่มีทรัพยากรเหลือน้อยหรืออุปกรณ์ที่มีไดรเวอร์ไม่ดีหรือปัญหาด้านอื่นๆ ที่เกี่ยวกับฮาร์ดแวร์


BrowserSource
Browser source is one of the most versatile sources available in OBS. It is, quite literally, a web browser that you can add directly to OBS. This allows you to perform all sorts of custom layout, image, video, and even audio tasks. Anything that you can program to run in a normal browser (within reason, of course), can be added directly to OBS.


## BrowserSource
แหล่งเบราว์เซอร์เป็นหนึ่งในแหล่งอินพุตที่หลากหลายที่สุดอย่างหนึ่งใน OBS  

### ตัวเลือกต่างๆ ของ อินพุตแบบเบราว์เซอร์

รายการ | รายละเอียด
--|--
Local File (Checkbox): |บอกแหล่งที่มาหากคุณกำลังโหลดหน้าเว็บจากเครื่องคอมพิวเตอร์ที่กำลังใช้งานอยู่หรือจากเครื่องอืนๆ (จากอินเตอร์เน็ต)
Width| ตั้งค่าความกว้างวิวพอร์ตของหน้าเบราว์เซอร์
Height| ตั้งค่าความสูงวิวพอร์ตของหน้าเบราว์เซอร์
FPS| ตั้งค่า FPS สำหรับเบราว์เซอร์
CSS| โดยปกติ ค่าเริ่มต้นจะเป็นดังนี้ <br> ตั้งค่าพื้นหลังให้โปร่งใส <br> ลบระยะขอบบนเนื้อหา <br> ซ่อนแถบเลื่อน (ในกรณีที่หน้าเว็บแสดงผลใหญ่กว่าความกว้าง / ความสูงวิวพอร์ต)
Default CSS | body { background-color: rgba(0, 0, 0, 0); margin: 0px auto; overflow: hidden; }
Shutdown source when not visible (Checkbox) | เลิกโหลดหน้าเมื่อไม่เห็นแหล่งที่มาอีกต่อไป (โดยคลิกที่ไอคอนรูปตาเพื่อซ่อนหรือไม่อยู่ในฉากที่ใช้งานอยู่)
Refresh browser source when scene becomes active (Checkbox) |  รีเฟรชหน้าเมื่อเปิดใช้งาน (เมื่อเปลี่ยนมาเป็นฉากที่มีอินพุตแบบบราวเซอร์)
Refresh cache of current page (Button) |  รีเฟรชหน้าและเนื้อหาทั้งหมด 

### ข้อควรระวังในการใชงานอินพุตแบบ Browser
สำหรับเวบไซต์ที่มีการล็อกอิน บางครั้งอาจจะพบว่าหน้า Browser ไปค้างที่หน้าล็อกอิน เนื่องจาก OBS ไม่ได้ใช้ session เดียวกับ browser ตัวอื่นๆ   
ถ้าเจอกรณีนี้ อาจจะเลี่ยงไปใช้งานอินพุตอชนิดอื่นแทน 


Browser Source is fairly straight forward with its options.

Shutdown source when not visible (Checkbox): Unloads the page when the source is no longer visible (by clicking the eye icon to hide, or not in the active scene).
Refresh browser source when scene becomes active (Checkbox): Refresh the page when it becomes active (scene is switched to)
Refresh cache of current page (Button): CLicking this will immediately refresh the page and reload any content.
As Browser Source is based on CEF, any CEF flags (--enable-gpu for example) can be passed from the OBS Studio shortcut. A fairly comprehensive list can be found here


Color Source
As the name implies, this source creates a solid color for you to add to your scene. This can be used for things like background colors or even a global color tint by using the alpha channel.

Color Source has the following options:

Color: Allows you to set the color the source will display. This is also where you set any desired alpha.
Width/Height: This allows you to set the resolution of the source. The primary point of changing this would be to set an aspect ratio that matches your canvas display.

Display Capture
Display Capture is used to capture your entire monitor. The options here are few, with a selection for the display you wish to capture, and a checkbox to enable or disable showing of your cursor.

You can only add one display capture source per display. If you need your display in multiple scenes, make sure you use Add Existing!


Game Capture
Game Capture is one of the primary sources that many users will be looking to use. This Source lets you directly capture the game you are playing, so long as it's DirectX or OpenGL. Game Capture is the most efficient way you can add your games to OBS, and should always be tried first. There are only a very small number of games that do not work with Game Capture. If you have issues with it and cannot solve them on your own, stop by the support chat!

Once you add your Game Capture Source, you will need to select a few options that suit your current needs. First is the Mode.

Capture any fullscreen application
Capture specific window
Capture foreground window with hotkey
The first option, capture any fullscreen application, will automatically detect any game running fullscreen on your primary monitor, and add the video output to the Game Capture source in OBS. If you play your games fullscreen, this is the option you should choose. Note that if you only have a single monitor, alt+tabbing out of the game to check OBS will cause the game to stop rendering, so you won't see it show up in the OBS preview.

The second option, capture specific window, allows you to simply select the active game you want to capture. Window Match Priority lets you select which parameters will be used to separate the available windows. For example, if you have two clients of the same game running with the same executable name, but different window titles, changing the Window Match Priority to Window Title can be very helpful in selecting the proper game to be captured. Experiment if you have issues selecting the right game and see which works best for you.

The final option, capture foreground window with hotkey, lets you set a specific key to tell the Game Capture source which game you want to show up. This is very useful if you change games often during a stream, and you don't want to have to go back into the Game Capture properties every time to select your new game. The hotkey can be set under Settings -> Hotkeys once the Game Capture source is added to your scene.

There are several other options, and we'll give a short description of them. In general, the default options are sufficient for most applications and you should not change them unless you know why you need to, and understand what they mean. As always, if you have any questions, please stop by the forums or chat.

Multi-adapter Compatibility: Used for systems that have multiple GPUs (such as a laptop). It changes the capture method from shared texture capture to memory capture. Memory capture is far less efficient than shared texture capture, and this option should only be enabled if you have no other options.
Force Scaling: Allows you to force a scale on the capture source.
Limit capture framerate: Limits the Game Capture source from capturing at a frame rate higher than OBS it set to use.
Capture Cursor: As implied, this will either show or hide the mouse cursor in your game. Does not apply to mouse cursors rendered in the game itself, those will always be captured.
Use anti-cheat compatibility hook:
Capture third-party overlays (such as steam): If your game has an overlay that doesn't conflict with Game Capture, this will allow Game Capture to capture it as well.

Image
This source allows you to various image types to your scene. Most image formats are supported. Alpha channel support is also available where applicable.

The only options in Image Source are the path to the image, and unload image when not showing. This checkbox will unload the image from memory while it is not active, which can be useful if you have a large amount of images and few system resources available.

Image Source supports the following image formats: .bmp, .tga, .png, .jpeg, .jpg, and .gif.


Image Slide Show
The Image Slide Show Source allows you to add multiple images that will rotate through as a slide show. To use this source, click the + sign to add either individual files or directories to be loaded. Once you have all the images you want, you can configure how you want them to display.

Transition: This drop down box allows you to select the animation type that will play during a transition between files. The default is a simple fade, but it can be changed to a cut, slide, or swipe
Time Between Slides (milliseconds): As the name implies, the time each image will be displayed before initiating a transition to the next.
Transition Speed (milliseconds): This is how fast the transition animation will take to go from starting to completely changed to the next image.
NOTE: This value does not increase the time between slides. For example, if you have the Time Between Slides set to 10000ms, and the Transition Speed set to 2000ms, the transition will BEGIN at 8000ms from the end of the last transition, with the next slide being fully visible at 10000ms. If this value is HIGHER than the Time Between Slides, it will automatically reduce the time to match. It also cannot be lower than 50ms.
Randomize Playback (checkbox): This option will let you choose if you want to randomize the images being played. If this is enabled, the next image will be randomized at each transition. If disabled, they will be shown in the order of the file list.
Image Slide Show Source supports the following image formats: .bmp, .tga, .png, .jpeg, .jpg, and .gif.


Intel® RealSense™ 3D Camera GreenScreen
This source type will allow you to use the digital green screen features of an Intel RealSense camera. RealSense cameras have a combination of a normal camera, infrared lasers, and an infrared camera to map the space in front of your PC and detect which parts of the video can be removed in a green screen effect. There is no configuration necessary for this source, simply add the source, pick your camera, and watch the magic!


Media Source
Media source is a great option to add all sorts of different media types to your stream. The currently supported file types are:

Video: .mp4, .ts, .mov, .flv, .mkv, .avi, .gif, .webm
Audio: .mp3, .aac, .ogg, .wav
Simple click the Browse button to select your file, or uncheck the "Local file" box to allow a URL or other remote location to be added. For remote files, the URL/path goes in Input, and generally Input Format can be left blank.

Once the file has been selected, there are only a few options that would need to be looked at.

Loop: Sets if the file will loop back to the beginning once playback has completed. Useful for .gifs
Restart playback when source becomes active: This will allow you to set the file to restart once the source is active. Active means in the current visible scene
Use hardware decoding when available: Fairly self explanatory!
Hide source when playback ends: If enabled, the source will automatically hide itself when the file has completed playback. Useful for video files so they do not show the last frame indefinitely.
Advanced: These options should only be access by users who understand what they are, and why they need them, so they will not be covered in this guide.

Scene
This Source is often overlooked, and while one of the simplest in function, it can allow for some of the most powerful functionality in OBS Studio. Since all Scenes are considered Sources, you can add an entire Scene as a Source anywhere you want.

For example, this can allow you to create a static overlay that you want to use in every Scene, called Overlay. In several other scenes, let's say Main and Game, you can add the Overlay Scene. If any changes are necessary to any of the Sources in Overlay, you can just update them it will be updated everywhere else. This is just one of many examples on how this Source type can be used!


Text (GDI+)
Text source can allow you to add simple text renders to your stream or recording layout. To get going, most of the default settings will be fine (except maybe the colors), and you can just type what you want your text to say in the field labeled "Text."

If you want to load the text from a file, simple check the "Read from file" checkbox, and select the file that has the text you want to read in it. The file must be UTF-8 (most default text files will be), and the file will be reloaded on save. This means you can edit the file and it will automatically update.

Once the text is present, there are quite a few options for styling it. You can:

Change the foreground color
Change the background color
Add a gradient
Adjust the opacity (transparency/alpha)
Set the horizontal and vertical align (relative to the red source bounding box)
Add an outline (with options for size, color, and opacity)
Use custom text extents for the size of the source, as well as if the text should wrap if the width is exceeded.

VLC Video Source
Similar to Media Source, you can add video and other media files to this source to be played in your scenes. This source type will use the VLC libraries for extended media support over the built-in Media Source. It requires that VLC be installed on your system to show up as an available source in OBS. If you are using 64bit OBS, you must install 64bit VLC and if you are using 32bit OBS, you must install 32bit VLC.

To add files, click the + sign to browse to your file, directory, or URL that you wish to add. If you add multiple, they will be played in the order they were added. If Loop playlist is checked, the playlist will start over once the end is reached.

The Visibility behavior drop down menu allows you to choose how visibility affects playback of the files. They should be self-explanatory.


Video Capture Device
The Video Capture Device Source allows you to add a variety of video devices, including but not limited to webcams and capture cards. On Windows, for a device to work with OBS the drivers needs to support DirectShow output. Since DirectShow is the standard output format for Windows, there's a good chance that this is what your device outputs. All major webcams and capture cards support DirectShow and will work with OBS.

To add your device, simply add the Source, open the properties and select your device from the Device drop down list.

You then have several options to configure it:

Deactivate/Active (Button): Clicking this will either turn your device off (when it reads Deactivate) or on (when it reads Activate).
Configure Video (Button): This button will open any driver configuration utilities. For example, with a Logitech webcam it will open the Logitech camera configuration software for enabling custom options like facial tracking. With a capture card, it might open the options to configure the input resolution and FPS.
Configure Crossbar (Button): Opens the device's Crossbar Configuration, if available. Consult your device's manual for more information.
Resolution/FPS Type: Most of the time this can be left on Device Default. If you are having issues with your device showing up, change it to custom and the following options become available to set manually:
Resolution: This sets the base resolution for the video device. Make sure it's a mode that your device supports!
FPS: Sets the FPS of the device.
Video Format: If your device supports multiple video output formats (Such as MJPEG or XRGB), you can select the preferred format here.
YUV Color Space: Sets the color space the device will output in.
YUV Color range: Sets the color range the device will output in.
Buffering: This has three different modes, Enable, Disable, and Auto-Detect. Enable will turn buffering on, which can help if you are getting stuttering during playback. Setting to Disable will turn buffering off, which can help if you are experiencing a delay on the device. Auto-Detect is recommended, as it will attempt to ask the device which method is preferred.
Flip Vertically (Checkbox): Flips the video image vertically. Some devices will (rarely) send the video input upside down.
Audio Output Mode: You can set to Capture Only (meaning you will not hear, without Audio Monitoring), or Output desktop audio (DirectSound/WaveOut). Enabling desktop output will send the device's audio out through your system default device.
Use custom audio device (Checkbox): When enabled, the Audio Device selection becomes available, and allows you to use a separate audio device that will be linked to your video device. This can be useful if you want to use an external microphone on a webcam, for instance, and want to tie the audio directly to the Source itself.

Window Capture
Window Capture allows you to capture a specific window and its contents. The advantages to using this source over Display Capture is that only the selected window will be shown, even if there are other windows in front of it (WIN7 NOTE: Having Aero disabled can interfere with this functionality.).


Deprecated Sources
List of currently deprecated sources. Sources listed here should not be used unless aboslutely necessary, and are only left in for backwards compatibility reasons.

Text (FreeType2)