#SUPERTRIO: requirements of the system for indoor location




##*Super Trio IPS*






###Team members 

#### *Somar*
#### *Ermias*
####*Bikash*

Date *08-12-2013*

Version *1.0*


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

======


### Use cases

Our product **Super Trio** has three primary actors, those are registered user, administrator, and visitor. Their accessibility on the application depends on what kind of user type and the credentials that the user is logged into. 
   
| User type       |   Definition        | User Cases |
| -------------   |:-------------:| -----:|
| **Administrator**      | `Owner of the Application  ` | *Add features*, *Edit the product*, *Delete regitered user account*, *Post and Comment*, *View contents*|
| **Registered User**      | ` a user with profile and access to most parts of the Application`    | *Log in*, *Browse or search*, *Find friends*, *Find locations*, *Edit account*, *Delete account*, *Log out* |
| **Unregistered User** | `Guests to the application  `    | *Contact the Administrator*, *Register*, *View Contents*|
       Figure 1, User cases chart

##User Case Diagram

In this picture is shown the role of all users and their relationships.

![Grbl Pin Diagram](http://users.metropolia.fi/~ermiash/user_case_diagram.PNG)

     Figure 2, Super Trio User Case Diagram

##System architecture

###Main modules/how do they function?

* Authentication

Super Trio is using two types of custom authentication modules: Credentials authentication modules and HTTP authentication modules. The credentials modules are used to check the credentials that the user types in the login form on the login page, as well as they are used when the visitor reaches the register form on the register page and fill in the blanks with the credentials. The HTTP modules are used to authenticate a user by HTTP request without showing the loging page.

* WifiLocationing

WifiLocationing is the module that defines Super Trio fundamental mechanism. WifiLocationing functional process is divided over two tactics. The first tactic insists on recognizing all the location points within the network that Super Trio is used in. The second tactic comprises the application functionality and the user need. It locates the user position and their destination with a touch of a finger, and takes them to the needed path page.

* Post

The post module can be mainly used by the administrator and the registered users. Both of those actors have the ability to check the contents, improve it, or comment on it.
The post module checks the the information that has been entered by the administration or the registered user in the post form that is found on several pages in the Super Trio, and then exhibits it in a user-friendly distinct form that gets along with Super Trio interface.




##User interface

####Main page

When you download SUPERTRIO and enter it, a main page full of several features will stop you. The main page insists
on a main navigation part where you can press Sign in to be taken to the signing in page, or Sign up to be taken
to the signing up form. The rest of the main page has the logo of the app, and several links for some recommended profiles where you can press on them and check these profiles without any ability for posting or commenting if you
are not a user.

####Sign up page

