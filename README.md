# iMessage Music Link Converter

(For the project board, refer to the "Projects" tab above) 

### Team Members ###
* Alex St.Clair
* Juvenal Arellano-Santana
* Natnail Getachew Belete

## Project Abstract
I have experienced many times the situation where I use a different music streaming platform than my friends, but want to send them a link to a song/artist. Currently, I have to go into the other platform, make a search, and find the song/artist to share with my friends. 
My project will take the form of a standalone iOS Message App Extension, and will take from the user a link to a certain song or artist on either Spotify or Apple Music, and not only translate that link to one from the alternate platform, but also send that new link straight to the other person in an iOS Message. This will use Web APIs for both platforms as well as the framework used to create iMessage extensions. 

![Use Case Image](https://github.com/3296Spring2020/individual-subject-proposal-tug89508/blob/master/StClair_iOS-URL-Converter.png)

### Vision
For people who use Spotify but whose friends use Apple music (or vice versa) and need a way to quickly and easily share music, artists, or albums, the iMessage URL Converter will let the user enter a link from their own platform and have that link translated to a link in another platform. Many users of these streaming platforms would have to remember the name of song/artist that they want to share, recall that information when entering the other platform, finding the same data, and using that application to send the data through iMessage. But with this application, this process is automated, leaving the user of the sole responsiblity of pasting the URL in any platform into the text box and pressing the button. 

### Persona
1. Jason is a 20 year old college student. He has owned exclusively Apple products since he was old enough to own one, and studies business at his local university. He is very interested in music and spends many hours a day with headphones in listening to his playlists on Apple Music. For his friends who also use Apple music, he often sends them songs and artists from his playlist. Since he does not have Spotify installed on his iPhone, he refers to sending Youtube links of these artists to friends who use Spotify. He needs a product like this so that he is able to more easily send music to all of his friends, not just the ones that use the same platform as him.

2. Emma is a 49 year old mom a husband and two children. She works in an office, where she often plugs in some headphones and listens to her daily playlists recommended to her by Spotify. She claims to not be knowledgable about apps or technology in general, and sometimes asks her children how to use features on her phone. For her, simplicity is key in creating a usable and intuitive application. Her co-worker has similar taste in music, but neither of them are able to find a way to share the music back and forth, other than watch Youtube music videos together in front of one of their work computers. Although they use different platforms, they both could install this app to solve the problem for both of them. 

3. Charlie is a 30 year old developer. He attended a large university for Computer Science, and is currently working on his own web Application. He is creating a website that utilizes some data from Apple Music when the user inputs an Apple Music Link, but the data that he is using to test the site is on Spotify. It is becoming tedious for him to check the name on Spotify, move to Apple music, search the same song, and then copy the link. He can use this application to first translate the Spotify link to the Apple Music link, before inserting the link into his website for processing. Since the process of sending the link is not necessary for the Application, he can simply use the app to translate the link and copy the new link. 


## Project Relevance
As far as the goals for this assignment, the following will certainly be fulfilled:

* Object Oriented Design 
* Test Driven Development 
* Unified Modeling Language (UML) 
* Debugging
* Code profiling and optimization
* Graphic User Interface

More goals from the slides may also be implemented as they may be needed, but the program will be written in Swift, an object-oriented language that will be used to create a graphic user interface. We will aim to follow test driven development as we add features to the application, to prevent breaks in the code. UML diagrams may be used, similar to the one above which demonstrates the workflow of the application. Debugging is inevitable, and will inherently appear in this project, as well as code optimization. 

## Conceptual Design
The problem that my application is aiming to solve is the cross-reference of URLs in common streaming platforms. Instead of having to visit another platform to retreive a link to a song/artist, my proposed application will appear in the application tray in iMessage to any user who has downloaded the application and has a conversation open. When the app is launched, a text box will appear, prompting the user to enter a link into the text box. Once entered, a function will be called to parse the link and determine its source (currently restricted to Apple Music and Spotify). The program will form a query in the web API of the posted link to gather details about the song/artist. After gathering this data, the program will then form another query in the API of the other application to retreive the URL for the same song/artist in the other platform. A list of results will appear for the user to confirm, and once confirmed, the program will automatically send the link to the recipient/recipients of the open conversation. 

### Feature list
This app is very simple and has a very concise objective, as defined below.
* Translate links from Spotify to Apple Music
* Translate links from Apple Music to Spotify
* Send the new, retrieved link to the recipient of the iMessage conversation

## Background
Attached is a link to the github repo. Xcode must be used to work on the project. After downloading the code, simply go to file->open->urlconverter. To run, click on the play button on the top left of the screen.

[https://github.com/3296Spring2020/individual-subject-proposal-tug89508/](https://github.com/3296Spring2020/individual-subject-proposal-tug89508/)

***Building***
- As stated above, Xcode must be used for this project. Since we are using swift, Xcode will have all of the resources that we will need.
- Allow plenty of time for the first build. Setting up the emulator does take a bit of time, especially if you are now using Xcode for the first time. 
- Here are the instructions:

1. Download and instal Xcode (and locate your Xcodeprojects folder)
2. Then go to GitHub, click clone or download on the repo, then download ZIP. 
3. Extract folder and place folder in Xcodeprojects
4. Rename the folder “urlconverter” (it gets renamed when you download from github
5. Go back to Xcode, and go to File -> open -> urlconverter
6. It will ask if you want to open, confirm this. You will not have to do this every time.

**Running**
- The run button is the play button on the top left, as stated  in "Background". This also takes time to start up, so please be patient. Once the emulator is open, navigate to one of the conversations in messages and select the unedited icon (white with a gray grid) from the iMessage app tray. This will open the first screen. 
- Given that we are working on the newest version of Swift, the suggested emulator to use is one of the newer iPhones. The simulator seems to be buggy with iMessage applications, I found that using an iPhone 8 (the oldest device that supports the newest Swift) performs more seamlessly. 

## Required Resources
* Group member's competencies
* Xcode 11.3.1 on Macbook (older versions may or may not work, but the version I am using is 11.3.1. Xcode is a Macbook exclusive, but VMs do exist. Macbook preferred.)
