<div style="float: center"><img src="http://users.metropolia.fi/~soumars/SuperTrio_logo.png" /></div>

#SUPERTRIO: requirements of the system for indoor location (community service)



##*Super Trio IPS*






####Team members: 
 1. Soumar Saloum
 2. Ermias Hailemichael 
 3. Bikash Sharma

####Date:
  *08-12-2013*

####*Version 1.1*


##Introduction

###Overall description


This printed material is a software requirements gathering and analysis for the project of indoor positioning application from the perspective of community services. 
<dl>
  
<dt>And the printed material includes :-   </dt>  
              
* System requirements
* User cases and diagram 
* Predictions of how it should be operated
* Analysis by trial and error

 

**The Super Trio** indoor positioning is as its name implies an application that helps a user to get the direction  in the school premises and provides the best way to get the user into his or destination. Positioning can be used to track where the person, who is assigned to do community service by attaching a tracking device in their body parts but that acquires GPS and the indoor positioning only works by using WiFi because of its weakness to detect large geographical locations as in the GPS devices does. And **Super Trio** can be used to control students in a detention room in a high school or elementary if not higher educational institution. 

The global positioning system has been used in most area of fields and locations but where the GPS can't reach, we need to use IPS because walls and roofs shields back the satellite signals which GPS relies on and that makes IPS the one and only option to gather and utilize information about a certain  premises.


Our first priority is to take the invasion of privacy risks into hands by only letting  trusted users in by using different methods of risk eliminators such as setting the WiFi set up so that guests can only use the WiFi of the school. The other one is protecting the profile of the user so that it can not be used otherwise by intruders.

How it works and what is needed :-
+ A compatible smart phone
+ WiFi connection 
+ Simple skill of computing 
+ Some information of the the destination or the person the user is looking for

The application runs in different platforms such as *iOS* , *Android* and *Windows phone*. Our main objective is to built an application with no usability problem issues, helpful and quick to fetch information when used within a small area network or in an institution with a large compound.
                                                    
======


### Use cases

Our product **Super Trio** has three primary actors, those are registered user, administrator, and visitor. Their accessibility on the application depends on what kind of user type and the credentials that the user is logged into. 
   
| User type       |   Definition        | User Cases |
| -------------   |:-------------:| -----:|
| **Administrator**      | `Owner of the Application  ` | *Add features*, *Edit the product*, *Delete regitered user account*, *Post and Comment*, *View contents*|
| **Registered User**      | ` a user with profile and access to most parts of the Application`    | *Log in*, *Browse or search*, *Find friends*, *Find locations*, *Edit account*, *Delete account*, *Log out* |
| **Unregistered User** | `Guests to the application  `    | *Contact the Administrator*, *Register*, *View Contents*|
       Figure 1, User cases chart
======
##User Case Diagram

In this picture is shown the role of all users and their relationships.

![Grbl Pin Diagram](http://users.metropolia.fi/~ermiash/user_case_diagram.PNG)

     Figure 2, Super Trio User Case Diagram


##System architecture

###High-level overview of the system

**The Super Trio** is an indoor loctioning application that helps students and teachers in educational facilities to find their way to several destinations inside the network they are studying/working in. The application is based on creating a social networking atmosphere up to serving the specified community by sharing location and making life easier and faster. The admin of the application can edit its features and implement new characteristics for it. The registered user is empowered by all the possible privileges of location sharing, finding a local destination, posting, commenting, and uploading photos. The visitor can only register if they want, contact the admin, and access a page to read about the application main idea.

###Main modules and their functions represented

* Authentication

Super Trio is using two types of custom authentication modules: Credentials authentication modules and HTTP authentication modules. The credentials modules are used to check the credentials that the user types in the login form on the login page, as well as they are used when the visitor reaches the register form on the register page and fill in the blanks with the credentials. The HTTP modules are used to authenticate a user by HTTP request without showing the loging page.

* WifiLocationing

WifiLocationing is the module that defines Super Trio fundamental mechanism. WifiLocationing functional process is divided over two tactics. The first tactic insists on recognizing all the location points within the network that Super Trio is used in. The second tactic comprises the application functionality and the user need. It locates the user position and their destination with a touch of a finger, and takes them to the needed path page.

* Post

The post module can be mainly used by the administrator and the registered users. Both of those actors have the ability to check the contents, improve it, or comment on it.
The post module checks the the information that has been entered by the administration or the registered user in the post form that is found on several pages in the Super Trio, and then exhibits it in a user-friendly distinct form that gets along with Super Trio interface.


##Requirements

###Functional requirements

- Trio.open: On the openning page the system shall give options for both registered users and visitors, whether they want to login or register.
- Trio.register: The system shall move the visitor to the register page and show a registeration form to be filled
- Trio.login: The system shall move the registered user to the login page where the user can fill in their credentials and login.
- Trio.fault: When a visitor is trying to register and fail to follow the requirement of any of the registration fields that should be filled, the system shall give a warning to fix the fault.
- Trio.missing: When a visitor is trying to register and misses any of the required registration fields that should be filled, the system shall give a warning to fill in the missing blank.
- Trio.submit: After a visitor fills in all the required fields in the registration form and presses submit, the system shall redirect them to message page says that they will recieve a confirmation email, and the system shall send this email automatically the registering visitor's email.
- Trio.login.smart: If a registered user types the correct email that correspondes their account but a wrong password, the system shall recognize the user and ask if the user wants to be redirected to the "forgot my password" form.
- Trio.login.pass: The user who is trying to login and types incorrectly the email or the email and the password together shall be asked by the system if they want to be redirected to the "forgot my email" form.
- Trio.logo: The system shall always redirect the user and the visitor to the main page when they press on the Super Trio logo in any page, and the contents of the main page is diverse depending on whether a registered user or a visitor pressed.
- Trio.alwaysLogged: In the login form, the user has an optional box to check, and by checking that box the user assures that they want to be always logged in whenever they open Super Trio. The system shall apply this function when the user checks the box.
- Trio.showLoc: The system shares the location of the logged in user.
- Trio.hideLoc: The system does not share the location of the logged in user.
- Trio.find: The system finds the location of any recognized point inside of the network coverage.
- Trio.search: The logged in user can search for any other registered users like them, and the system shall find them by name or email.
- Trio.takeMe: The system shall show the registered user the path they need to find the needed destination from their own location.
- Trio.post: The logged in user can post letters thier own location.
- Trio.upload: The logged in user can upload their photos to their account.
- Trio.edit: The system lets the logged in user to edit their own account.
- Trio.accPic: The registered user can upload, change, and edit a picture for their own account.
- Trio.usrnme: The logged in user is able to give themselves a username.
- Trio.contact: The registered user and the visitor can contact the admin of Super Trio by filling the contact form.
- Trio.faq: The registered user is able to go to FAQs page to find some help concerning Super Trio.
- Trio.feedback: The registered user may reach the feedback form to fill and send feedback to the admin.
- Trio.abtUs: The visitor can know about Super Trio by visiting About Us page.
- Trio.comment: The logged in user can comment on any other shared locations posts of their friends by filling the comment input under each post.
- Trio.plus: The logged in user can give a plus point to any of their friends by pressing on the plus sign (+) under any of their friend's posts.
- Trio.connect: The registered user can connect their account to facebook to recieve some info to their Super Trio account, like account picture and gender.
- Trio.prof: The registered user can specify their profession to make other users in Super Trio network know their site of express.

###Non-functional system requirements

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

###Other non-functional requirements

####Readability:

It specifies the good visibility of the fonts, and the ease of perceiving the items on the system interface.

####Accessibility:

Helps to identify some of the system functionalities. It can also serve tips that assist in identifying features in the system software for users with disabilities.

####Scalability:

It specifies the ability of the system to continue functioning well, in order to maintain the user satisfaction, when the size or volume of data being imported to the system is getting bigger and heavier.


##User interface

####Main page

When you download SUPERTRIO and enter it, a main page full of several features will stop you. The main page insists
on a main navigation part where you can press Sign in to be taken to the signing in page, or Sign up to be taken
to the signing up form. The rest of the main page has the logo of the app, and several links for some recommended profiles where you can press on them and check these profiles without any ability for posting or commenting if you
are not a user.

####Sign up page

