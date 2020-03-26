

This application will help in the process of contact tracing patient in an automated and semi automated way respecting privacy. This aplication uses bluetooth for generating the contact information. 
This application is made in order to help normalize the current situation with covid-19, but in the future can help with the containment of other diseases.

** The initial version of this application will target the folling actors:**
- Individuals, installing the mobile aplication, self identifying, input basic medic information (not transmitted) ,  and generating the "contact" information. 
- Goverment agencies trying to control the public health problem and managing citizen data and privacy. 
- Medical teams identifying cases and generating tracing events. 
- Researchers working over anonymized data, exploring ways in order to get a more accurate trace data and even predicting cases ahead of time. 

** The principles of the application ** 
- Secure and anonymous. 
- Adaptable to different privacy and legal frameworks
- Auditable to avoid bad actors. 

** The non functional requirements **
- Low battery consumption on mobile devices
- High compatibility on the mobile part. 
- Plataform neutral data in order to adapt to multiple server frameworks. 
- Easy to customize in order to adapt to different enviromentms 
- Scalable to millions of users and billions of "contacts"

** The aproximate user history of the apo: **
- You enroll to a public service that give you a cripto token, similar to your run of the mill cyrptocoin wallet.
-  You input your relevant medical information, including if you were already infected and cured, and comorbities (age, weight, smoking habits and other medical related issues). People can lie here, but it just a reference value. This information is not transmitted to anywhere other than the phone.
-  Use bluetooth, without pairing you can sense the proximity nerby beacons to determine who is close to you. A reverse flight mode should be implemented, meaning bluetooth radios must be on. I don’t think pairing is necessary, we can intervene earlier in the protocol
-  Every time you “contact” a bluetooth signal, an event is generated with the proximate time and strengh. A combined hash is generated with your bluetooth mac or BD_ADDR. The event hash is send to a server with your token, the other person will send a similar hash in a way both can be linked but not traced at the moment
-  If you get cornavirus, medical team generates a certificate to “open” your trace contact history, The server version contact trace the events to the particular day of the supposed infect and alerts the users via the “wallet”.
Once you get cured, medical team puts another token on your wallet, suspecting you cannot get reinfected or pass it to other people.


This is a basic diagram of the interaction between the different actors
![Image of General Model](https://github.com/jotatsu/Digital-Shield/raw/master/Modelio/General%20Communication%20Model.png)

Person enrollment:
![Image of Contact trace request](https://github.com/jotatsu/Digital-Shield/blob/master/Modelio/Enrollment.png)

Contact event generation:

![Image of Contact trace request](https://github.com/jotatsu/Digital-Shield/blob/master/Modelio/Generate%20Trace.png)

Contact trace request

![Image of Contact trace request](https://github.com/jotatsu/Digital-Shield/blob/master/Modelio/Generate%20Contact.png)
