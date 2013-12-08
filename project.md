![Logo](http://users.metropolia.fi/~soumars/SuperTrio_logo.png)

#SUPERTRIO: requirements of the system for indoor location (community service)

##*Super Trio IPS*

####Team members: 
 1. Soumar Saloum
 2. Ermias Hailemichael 
 3. Bikash Sharma

####Date:
  *08-12-2013*

##Table of Contents 

**1. Introduction**

 1.1 Overall description

**2. Use cases**

 2.1 Definition of the user groups
 
 2.2 Use case diagram

**3. System architecture**

 3.1 High-level overview of the system
 
 3.2 Main modules and their functions represented

**4. Requirements**

 4.1 Functional requirements
 
 4.2 Non-functional system requirements
 
 4.3 Other non-functional requirements

**5. User interface**

 5.1 Visitor
 
 5.2 Registered user
 
 5.3 Administrator

**6. Project management**

##1. Introduction

###1.1. Overall description

This printed material is a software requirements gathering and analysis for the project of indoor positioning application from the perspective of community services. 
<dl>
  
**And the printed material includes:**
              
* System requirements
* User cases and diagram 
* Predictions of how it should be operated
* Analysis by trial and error
* User Interface of all known users

**The Super Trio** indoor positioning is as its name implies an application that helps a user to get the direction  in the school premises and provides the best way to get the user into his or destination. Positioning can be used to track where the person, who is assigned to do community service by attaching a tracking device in their body parts but that acquires GPS and the indoor positioning only works by using WiFi because of its weakness to detect large geographical locations as in the GPS devices does. And **Super Trio** can be used to control students in a detention room in a high school or elementary if not higher educational institution. 

The global positioning system has been used in most area of fields and locations but where the GPS can't reach, we need to use IPS because walls and roofs shields back the satellite signals which GPS relies on and that makes IPS the one and only option to gather and utilize information about a certain  premises.

Our first priority is to take the invasion of privacy risks into hands by only letting  trusted users in by using different methods of risk eliminators such as setting the WiFi set up so that guests can only use the WiFi of the school. The other one is protecting the profile of the user so that it can not be used otherwise by intruders.

**How it works and what is needed:**

+ A compatible smart phone
+ WiFi connection 
+ Simple skill of computing 
+ Some information of the the destination or the person the user is looking for

The application runs in different platforms such as *iOS* , *Android* and *Windows phone*. Our main objective is to built an application with no usability problem issues, helpful and quick to fetch information when used within a small area network or in an institution with a large compound.

##2. Use cases

###2.1. Definition of the user groups

Our product **Super Trio** has three primary actors, those are registered user, administrator, and visitor. Their accessibility on the application depends on what kind of user type and the credentials that the user is logged into. 
   
| User type       |   Definition        | User Cases |
| -------------   |:-------------:| -----:|
| **Administrator**      | `Owner of the Application  ` | *Add features*, *Edit the product*, *Delete regitered user account*, *Post and Comment*, *View contents*|
| **Registered User**      | ` a user with profile and access to most parts of the Application`    | *Log in*, *Browse or search*, *Find friends*, *Find locations*, *Edit account*, *Delete account*, *Log out* |
| **Unregistered User** | `Guests to the application  `    | *Contact the Administrator*, *Register*, *View Contents*|
       Figure 1, User cases chart

###2.2. Use case diagram

This illustrative diagram shows the role of all users and their relationships.

![Grbl Pin Diagram](http://users.metropolia.fi/~ermiash/user_case_diagram.PNG "User Case Diagram")

     Figure 2, Super Trio User Case Diagram

###2.3 User case scenerio

![scenerio](http://users.metropolia.fi/~ermiash/super_trio/scenerio.PNG "Register case scene")
 
   Figure 2.1, User case scenerio
##3. System architecture

###3.1. High-level overview of the system

**The Super Trio** is an indoor loctioning application that helps students and teachers in educational facilities to find their way to several destinations inside the network they are studying/working in. The application is based on creating a social networking atmosphere up to serving the specified community by sharing location and making life easier and faster. The admin of the application can edit its features and implement new characteristics for it. The registered user is empowered by all the possible privileges of location sharing, finding a local destination, posting, commenting, and uploading photos. The visitor can only register if they want, contact the admin, and access a page to read about the application main idea.

###3.2. Main modules and their functions represented

* Authentication

Super Trio is using two types of custom authentication modules: Credentials authentication modules and HTTP authentication modules. The credentials modules are used to check the credentials that the user types in the login form on the login page, as well as they are used when the visitor reaches the register form on the register page and fill in the blanks with the credentials. The HTTP modules are used to authenticate a user by HTTP request without showing the loging page.

* WifiLocationing

WifiLocationing is the module that defines Super Trio fundamental mechanism. WifiLocationing functional process is divided over two tactics. The first tactic insists on recognizing all the location points within the network that Super Trio is used in. The second tactic comprises the application functionality and the user need. It locates the user position and their destination with a touch of a finger, and takes them to the needed path page.

* Post

The post module can be mainly used by the administrator and the registered users. Both of those actors have the ability to check the contents, improve it, or comment on it.
The post module checks the the information that has been entered by the administration or the registered user in the post form that is found on several pages in the Super Trio, and then exhibits it in a user-friendly distinct form that gets along with Super Trio interface.


##4. Requirements

###4.1. Functional requirements

<b>Trio.open:  </b> On the openning page the system shall give options for both registered users and visitors, whether they want to login using login form or register.

<b>Trio.register:  </b>The system shall move the visitor to the register page and show a registeration form to be filled

<b>Trio.fault: </b> When a visitor is trying to register and fail to follow the requirement of any of the registration fields that should be filled, the system shall give a warning to fix the fault.

<b>Trio.missing:</b> When a visitor is trying to register and misses any of the required registration fields that should be filled, the system shall give a warning to fill in the missing blank.

<b>Trio.submit: </b> After a visitor fills in all the required fields in the registration form and presses submit, the system shall redirect them to message page says that they will recieve a confirmation email, and the system shall send this email automatically the registering visitor's email.

<b>Trio.login.smart: </b>If a registered user types the correct email that correspondes their account but a wrong password, the system shall recognize the user and ask if the user wants to be redirected to the "forgot my password" form.

<b>Trio.login.pass:</b> The user who is trying to login and types incorrectly the email or the email and the password together shall be asked by the system if they want to be redirected to the "forgot my email" form.

<b>Trio.logo: </b>The system shall always redirect the user and the visitor to the main page when they press on the Super Trio logo in any page, and the contents of the main page is diverse depending on whether a registered user or a visitor pressed.

<b>Trio.alwaysLogged: </b> In the login form, the user has an optional box to check, and by checking that box the user assures that they want to be always logged in whenever they open Super Trio. The system shall apply this function when the user checks the box.

<b>Trio.showLoc: </b>The system shares the location of the logged in user.

<b>Trio.hideLoc: </b>The system does not share the location of the logged in user.

<b>Trio.find: </b>The system finds the location of any recognized point inside of the network coverage.

<b>Trio.search: </b>The logged in user can search for any other registered users like them, and the system shall find them by name or email.

<b>Trio.takeMe: </b>The system shall show the registered user the path they need to find the needed destination from their own location.

<b>Trio.post: </b>The logged in user can post letters thier own location.

<b>Trio.upload: </b>The logged in user can upload their photos to their account.

<b>Trio.edit: </b>The system lets the logged in user to edit their own account.

<b>Trio.accPic: </b>The registered user can upload, change, and edit a picture for their own account.

<b>Trio.usrnme: </b>The logged in user is able to give themselves a username.

<b>Trio.contact: </b>The registered user and the visitor can contact the admin of Super Trio by filling the contact form.

<b>Trio.faq: </b>The registered user is able to go to FAQs page to find some help concerning Super Trio.

<b>Trio.feedback: </b>The registered user may reach the feedback form to fill and send feedback to the admin.

<b>Trio.abtUs: </b>The visitor can know about Super Trio by visiting About Us page.

<b>Trio.comment: </b>The logged in user can comment on any other shared locations posts of their friends by filling the comment input under each post.

<b>Trio.plus:</b> The logged in user can give a plus point to any of their friends by pressing on the plus sign (+) under any of their friend's posts.

<b>Trio.connect:</b> The registered user can connect their account to facebook to recieve some info to their Super Trio account, like account picture and gender.

<b>Trio.prof: </b>  The registered user can specify their profession to make other users in Super Trio network know their site of express.

###4.2. Non-functional system requirements

####Usability:

We think that the most important part to make our system well-known is to keep it simple and user-friendly. As of our experience in some other systems that work in the same field Super Trio works in, we noticed that the most issue that attracts the user is the fast easy start. We live in very fast world nowadays, and people are not patient as before for long procedures.

We summed up that the user won't leave us if they like, for example, the registering procedure, so, we are trying to focus on making the registering process easy and nice-feeling for the user. The filling form is easy and any normal human being can fill it in seconds. The confirmation email shall be in the user's inbox in seconds, as well.

When the user feels this easy dealing with our system, they will give a chance to dive more in our system's features. The user won't find hard time editing their account, nor sharing their locations. Everything is going to be on the main page. one press for going to edit the account, one press for sharing location, and one press for finding a needed destination, all from the main page.

####Reliability:

We think that our user will always be faithful to us if we really show that we are reliable. For that, we assure to our users a privacy-keeping with us, and that all their personal information are saved securely and no one can reach them except the user themsleves and the admin. Moreover, to assure more privacy, the admin cannot access the user's password in anyway, so, the user can be sure that no one but them knows their password.

In case of any incorrect information filling to the login form, the system will immediately give a message that warns the user to retype the email or the password in the right way or redirect themsleves to the "forget" forms if they forgot any of their credentials.

To maintain the user's privacy, we also give the user the ability to remove or delete from their renewable feeds any bothering or non-acceptable posts or pictures that injures modesty on their account main page or as a comment on one of their posts.

List of the possible system failures and how the system reacts to them:
  1. Incorrect email or password: The system asks to retype correct info or to redirect to the "forget" form.
  2. Bothering material: The system gives the ability to the user to delete such material from their feeds.
  3. Missing fields in the register form: The systems asks the visitor to fill in the blank fields.

####Efficiency:

As long as we are expecting that our product should be used and loved by a lot of people from different types and needs, we should provide some solutions to satisfy any kind of personality uses Super Trio.

Like we mentioned before, our system mostly is going to be used in the educational facilities, accordingly, we know that the biggest part of our possible clients are going to be of youth. The young generation nowadays don't want to wait until they share their location, upload a photo, or make a comment. We highly confirm that Super Trio server is a high-quality server that accomplishes any kind of function in a second or two.

Furthermore, to not make anyone reach us down, we provide in our About Us page all of the features that Super Trio provides and all the functionalities and utilizations of it. This way we can be sure that whoever wants to start with us will know if our product fits them or not.

###4.3. Other non-functional requirements

####Readability:

It specifies the good visibility of the fonts, and the ease of perceiving the items on the system interface.

####Accessibility:

Helps to identify some of the system functionalities. It can also serve tips that assist in identifying features in the system software for users with disabilities.

####Scalability:

It specifies the ability of the system to continue functioning well, in order to maintain the user satisfaction, when the size or volume of data being imported to the system is getting bigger and heavier.


##5. User interface

Depending on 3 different type of users, the user interface of SuperTrio will be displayed. 
First page for all 3 users will be same. It will be simply a page where they can login with username and password. Or/else go to register page.

![Grbl Pin Diagram](http://users.metropolia.fi/~bikashs/supertrio/firstpage.JPG "Face of the Super Trio")

                    Figure 3, Super Trio Login/visitor page
               
###5.1. Visitor

Visitor in this case are everybody who visit first page, therefore even other type of user have to go through visitors page. Even there's search box, but after search query is send, it again force to login, or register. 
So Visitor either login or click to Register. Where they are ask few basic info to enter and then they are converted to Registered users. 
![Grbl Pin Diagram](http://users.metropolia.fi/~bikashs/supertrio/register.jpg "Register Page")
               
                    Figure 4, Super Trio Register page
               
               
 ![Grbl Pin Diagram](http://users.metropolia.fi/~bikashs/supertrio/error.jpg "When an error occures")
 
                    Figure 5, Super Trio error page

###5.2. Registered user

These are the main target of our software. After getting username and password from register page, they can then again visit first page to login. After they login there are different option avilable. 
Welcome or main page consist of sidebar with option such as;option for managing settings such as changing privacy option, changing password, selection connection(wifi/internet) or deactivating account.Edit profile option for editing basic profile i.e username(displaying),profile picture, email. Visited/shared location for viewing location that are shared by user or has been tagged from other users.Friends list for listing all the friend added. Friend can be added by searching and just clicking + button near name.  And notifcation for viewing all active and old notification. Similarly main part of page consist of mainly a shared post(location) of friend which let user know where are/were there friends, top search box to search friend and location, and share option to share location and tag friends. 

 ![Grbl Pin Diagram](http://users.metropolia.fi/~bikashs/supertrio/usermain.jpg "Registered User page")
 
                    Figure 6, Super Trio main user page
    
  ![Grbl Pin Diagram](http://users.metropolia.fi/~bikashs/supertrio/settings.jpg "Registered User settings")
  
                     Figure 7, Super Trio settings page      

![Grbl Pin Diagram](http://users.metropolia.fi/~bikashs/supertrio/editprofile.jpg "Registered User profile page")

                     Figure 8, Super Trio  Edit profile page
          
![Grbl Pin Diagram](http://users.metropolia.fi/~bikashs/supertrio/location.jpg "Location")

                     Figure 9, Super Trio  Location page 
      
![Grbl Pin Diagram](http://users.metropolia.fi/~bikashs/supertrio/friends.jpg "Registered User friends")

                     Figure 10, Super Trio  Friends page
   
###5.3. Administrator

Administrator has many feature like registered user, but little bit in different way, eg: Registered user post their location to friends, but administrator can post to all users, and also he can share to certain targetted group according to desire. But post page looks same. Setting page has more settings, for controlling different feature, instead of friends page, admin has users list. Where he can select and delete users if needed. Notification icon for admin is disable since its not useful. Instead there's new icon called Add feature, from which admin can implement new feautre by just adding the app code. Mainly admin i.e Main admin controlls stuffs by coding from different server computer, so App admin normally has very limited stuffs to perform so it's not heavy.

![Grbl Pin Diagram](http://users.metropolia.fi/~bikashs/supertrio/admin.JPG "Administrator page")

                    Figure 11, Super Trio add feature of Admin page

##6. Project Management

We must admit that we have spent most of the project time discussing over what is best for the project while taking notes and setting up meetings to see the bigger picture and those meetings were later proven to give us the consequential result. We have discussions on subjects such as; should the presentation be more texual or pictorial? What kind of media should we use to define the application? What is the achievement goal and how can we grab it? What are we going to learn from this particular experience? etc. And the whole project has been a great learning experience for all of us.  

As newbies for software engineering and it's tools such as Github, we faced some difficulties of getting used to learn its ways. But as the hours we spend on it increased, the level of difficulty and vagueness started to decrease but we will need to spend some more time working on it on our own to see all the difficulties vanish.

Working hours ranged between 17-20 hours from each of us. The division of the documentation parts was totally fair for each one of us and everyone managed to do their job completely and on time.
