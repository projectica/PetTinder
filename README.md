# PetTinder - "Play the game, share the love, save a life" 

(I'm well aware the tag line is too sweet and earnest to be cool, and so expect this to change. For now, it encapsulates how it works, big-picture style.)   
  
The landing page for the game, and the email list for collaborators and future players:
https://projectica.org/pettinder-game/

How to play PetTinder:
https://paper.dropbox.com/doc/PetTinder-the-how-to-play-page--AMIdm548DfIbaK56Ug6uFox2AQ-HTyHV44EXQtQnAYZcTwzS

Resources for and about this project: 
https://github.com/janerette/PetTinder

Demo web app:	https://t.co/7GdDq7yZ2s	
Demo app code:	PetTinder_web	


# Technical Specifications  
PetFinder API documentation:	https://www.petfinder.com/developers/api-docs	
NPM package to call PetFind API:	https://www.npmjs.com/package/pet-finder-api	

## General App Description:
PetFinder is a huge database of adoptable pets looking for a new home. 

PetTinder will be a mobile game that connects to the PetFinder API.  The objective of the game for the user is a pleasant passtime with the virtuous side effect of raising funds for pet shelters; as well as be a research tool for adoption,  after the game version is complete.

The way it works has similarities with the Tinder app, hence its name: pictures of pets are displayed, and user can swipe them right or left. 

The app will be location based, and the pets displayed will be located within a 500km radius from the user. 

There will be a social share button on the Pet Presentation screen, so that user can share the pet on social networks before swiping. This is also a way to grant free plays and viral game shares, as it entices people to either join the game, or view the pet at its shelter.

When swiping right, more details are displayed about the pet, and this adds the pet to his/her list of Loved Pets.

User can decide between 5$ and 10$ per month to donate. There will be a slide for user to select which amount will be donated per swipe. For each pet on his Love list, user will be able to click a link and donate directly to this pet’s shelter.

User will have a Love list, where he/she can see the details of the loved pets and display the pet's details screen.

When a pet gets adopted, user will get notified, and this pet will disappear from his/her loved list.

There will be a leaderboard to list the users who gave the biggest amounts and shared the most pets.

There will also be an admin web console where the app admin can access the database, and some statistics reports.

## Screens description:			Screens can be seen from the How to Play PetTinder link above. This content was copied from and is available in a spreadsheet. 

### Splash Screen: 	

Specifications 

When pressing "Get started" button:		
If user is already registered, go directly to the Pet's screen	[Pet Screen	]
If it is user's first time, go to the Registration screens	Sign up/Registration screens	
Sign up/registration, sign in:	
registration screen 1:	Capture email and password, or allow Facebook registration	
registration screen 2:	Capture First Name and Last Name	
registration screen 3:	FUTURE DEVELOPMENT: Capture flag "adopt" if user clicks on "Adopt Button"	Specifications:	link	
 	
Once registration is finished, go to the Welcome Tour screens:	

### Welcome tour screens	
After registration, the following welcome tour screens shall be displayed:	 	

How to Play …
Share …
Your Love List …
When a pet is adopted …
The first x Loves are on us …
Get a donation receipt for your subscription


### Pet screen	
This is the first screen of the game.
Pressing on the top left Hamburger button shall display the app's menu	Go to App menu screens	
Pressing on the top right Player button shall display the user's profile.	Go to User's profile screens	

This is the screen diplaying the pet's  picture, name, gender and breed, as retrieved from the PetFinder API	

Specifications
Pets retrieved from the PetFinder API shall all be within a 500km radius from user's phone geolocation.	See PetFinder API documentation	
Pets which are on the user's discarded pets list shall be filtered out from the pets retrieved
Pressing  the 'X' button shall do the same as swiping left		
Pressing the heart button shall do the same as swiping right		
Swiping right or pressing the heart button will add this pet to user's Love list, and display the pet's complete profile	Pet's profile screens	
Swiping left or pressing the 'X' button will display another pet, and add the pet to the user's discarded pets list, so that this user doesn't see this pet again [until the Available Reset button is activated - later development]

FUTURE DEVELOPMENT: 
If user has a "foster" profile, an icon will indicate that a pet is available for foster (see right screen)		
Looking to foster logic: check if it is an option we get from the PetFinder API. If yes, then a special icon would be displayed on the pets who are available for fostering
Businesses who play the game will be able to "sponsor" a pet. All pets added to their Love list will display a badge with the business name (see left screen)		
The Share button shall be visible on the Pet screen, although it is not on the demo screens.		
Pressing on the top left button shall display the app's menu	Go to app menu screens	
Pressing on the top right button shall display the user's profile (see below)	Go to user's profile screens	

### Pet profile screens	
When user swipes right, the pet's detailed profile shall be displayed, and this pet shall be added to user's Love list	

Specifications:	Links	
Swiping left shall display another pet		
Swiping right shall display the next detail screen for this pet		
User shall also be able to share the Loved pet from this screen		
Pressing on the top left button shall display the app's menu	Go to app menu screens	
There will be as many "dots" displayed as pictures in the pet profile, so that user can swipe through all pictures provided.	
Pressing on the top right button shall display the user's profile.	Go to user's profile screens	

### User profile screens	
These screens shall be displayed when pressing the top right button, from all screens except the Welcome Tour and Registration screens	
Specifications:		

Your profile is editable by pressing the pen icon. The profile screen is scrollable to contain all fields 
Name 
Email address
Password

See your love list contains a horizontal row of icons representing pets. Selecting this row shows you a vertical scrolling list
Your badges - acknowledgement levels of game play, including leaderboard comparison with peers
See Back-end specs for description of badges		
The "Donation amount per love" section shall be a slider, where user can set the amount which will be donated per swipe. This affects the number of pets she can add to the love list each month. If she wants to add more, she can make a one-time top up donation of $5 or $10.		
The "Current plan" section is to determine user's monthly donation		
The "Payment method" section will be different from what is shown on the sketch: it will rather show a button to redirect user to payment methods (third-party app)		

FUTURE DEVELOPMENT: "Looking to foster" flag is what determines if user gets an indication of which pets are available for foster		
Pressing on "Reset pet list" button will delete the user's discarded pets list		

Pressing on "Delete account" shall delete this user account completely. It should first ask user "are you sure you want to delete your account?".		
There should also be an option to suspend the account. When user chooses this option, he will then get a pop-up to be able to choose a number of one to three months, or until user reactivates his account himself.		

## Menu screens (Hamburger options):	

### 1) Love list	

Specifications:	Links	
This screen shall display all pets retrieved from the user's Love list		
User shall be able to share any pet from the Loved list by pressing the share button.		
From any pet on the Loved list, there shall be a link to make a donation to that particular shelter (not shown on the print screen)		

// this needs editing… 
Pressing on the top right button shall display the user's profile.	Go to user's profile screens	

### 2) Welcome tour screens	
Same screens as above	
 
### 3) Leaderboard	

Specifications:	Links	
This screen shall display users in the same group. When user invites someone else to play PetTinder, he will see the invited user in his Leaderboard. The same way, if a user has been invited by another user, he will see the inviting user in his Leaderboard.	 	
The total amount donated by this user shall be displayed for each user on the Leaderboard	 	
Pressing on the top right button shall display the user's profile.	Go to user's profile screens	

### 4) About PetTinder	

Specifications:	Links	
This screen shall display information about PetTinder.	 	

### 5) Become a foster home	

Specifications:	Links	
This screen shall display information about why you should become a foster home, and how to use PetTinder to help you find a pet or shelter to foster for.	 	

### 6) FAQ (will contain a link to the web page)	Specifications:	Links	
(no example screen)		This screen will display a list a frequently asked questions and answers, and a link to the PetTinder's website, where a form will be available to ask new questions	


### Social media share button logic	
When user clicks on the share button, she will get the standard pop-up to choose on which media to share.	
There will be a default text "Hi, I way this pet on PetTinder and thought of you", with a variable containing the link to see this pet.	

## Back-end specs

//to develop

Donations either go directly to a foundation that then remits our expenses to us, or are held by us and sent to the foundation with donation reports.
Financial engine possibility: GetCheddar	getcheddar.com	

Once a month, donations shall be remitted to the charitable foundation, at a fixed date for all users. 
For each user, the first donation amount shall be calculated according to the user's registration date.
On an ongoing basis, and compiled quarterly, the database shall account for micro-donation amounts per pet, and per shelter, and consolidate donations across all users for shelters and their pets. 
This report will be remitted to the charitable foundation so they can cut a donation cheque to each shelter and report to the shelter which pets were of interest

Future development: On months when the user does not play the game but continues their charitable subscription, the donations shall be split (in up to 5¢ increments) according to the number of pets remaining in their Love list (a $5 donation can then support up to 100 pets). Each pet in their Love list will then get a coin icon for each month they were supported by a micro-donation.   
When receiving a request from a user who clicked on a link shared by another PetTinder user, the app will connect the user who clicked on the link to the user who sent it, so they both will become Peers (see each other) on their leaderboard.
Peers will be members who share similar rates of play and donation support.


## Persistent Data
 
## BETA TESTING

### User profile				  			  
userID		    			       	 
email		         	            	
First Name		  	    		  
Last Name		   			        	    
Foster flag		  				                               
Monthly donation
Donation per loved pet		 	
Total donated			
Register Date	
Last Login Date	
payment checked	
last location (GPS coordinates)	
Inactive flag	
Adopt flag	

### Love List
userID
petID		  
shelterID		
amount donated	
Date Loved

### Discarded Pets List	
userID	
petID	
shelterID	         
      
### Monthly Donations
userID
Amount	
petID 
shelterID
Year-month

### Donations 
shelterID	
petID
Year-month
Date sent
Amount	
      

## DELIVERY	
Leaderboard	
MainUserID	
FriendID


# Questions to answer / Ideas

Leaderboard: how might it work?	
How will the app get notified when a pet was adopted vs other status? Is it a field when retrieving pets from the API?
What do we want to see in the web console	(if any)?
Reports? Statistics?
report for beta:	
number of users	
total of subscription donations	
consolidated play report:	
shelter ID	Pet ID	donation total
Pet ID	donation total
shelter ID	donations total	E11
