## Actors
- Law Enforcement
  - Characteristics: Includes Police Officers and agencies. They may need to access drone activities for public safety and security and to help maintain the law. May want to have access to drone data to investigate potentional violations, threats, or spoofing activites.
- Government Officials
  - Characteristics:  Individuals with responsibilities of overseeing and regulating drone activities. Need to access drone data for security and compliance purposes. May want to access for concerns of legality and security of drone activities.
- Government Agenices
  - Characteristics: Government organizations responsible for managing and regulating drone operations. May coordinate with other users or actors to enforce regulations and ensure safety and security.
- Public
  - Characteristics: Individuals or operators who are interested in drone activities such as safety, privacy, or recreational concerns. May access for information of drones in the area. May have an interest in accuracy and security of drone data.
- Clients
  - Characteristics: Provide real-time or previous drone data collected. Can include future clients, drone manufacturers, or other data providers. Need access to ensure app is working properly and able to provide possible updates. Ensures data and systems are working properly in detection.

## Use Cases
**UC1: User creates an account**
- Connection: BR1
- Actors: Users
- Flow:
	1.User opens device
	2. User clicks on app
	3. User hits “Create an account” below the sign in button
	4. The user is then taken to a screen where they insert information such as their first and last name, phone number, and their email address.
	5. The user then hits submit after inputting their information.
	6. Email is then sent to the email address to confirm the account.
- Explanation: The application will store and protect this information for future user login attempts. This ties into the data curation framework because user login information, details, and activity will now be tracked within the app.

**UC2: User Signs into Application to Access Data and Map**
- Connection: BR1
- Actors: Users
- Flow:
    1.User opens device
    2.User Clicks on app
    3.User enters their username
    4.User enters their password
    5.User hits sign in and is then signed in.
- Explanation: The application will ask for authorization from the user to identify who is accessing the application. Provided the user has an account set up through the application, they will gain access to drone information and mapping,
  
**UC3: User needs to reset password for their account**
- Connection: BR1
- Actors: Users
- Flow:
    1.User opens device
    2.User clicks on app
    3.User clicks on "Forgot Password?" below the sign in button
    4.The application takes the user to a screen where they will insert their email.
    5.The user hits submit.
    6.A screen is shown stating a recovery email has been sent to their email provided.
- Explanation: The application will help provide additional security in the aspect of authorization. This will prevent people from accessing accounts that are not theirs and will help allow users access back into their accounts.

**UC4: User using an authenticator to access app**
- Connection: BR1
- Actors: Users
- Flow:
  1.	User opens device.
  2.	User clicks on app.
  3.	User enters their username/email.
  4.	User enters their password.
  5.	User then hits sign in.
  6.	The user is then sent to another screen where they enter a passcode from their authenticator of choice.
  7.	After the system registers the authenticator password, the user will then be directed to the drone map and drone list screen.
- Explanation: A user may want to have another layer of protection or may be required by their corporation to have an authenticator. There will be the availability of an authenticator being used to add in another layer of protection to ensure no one is accessing someone else’s account.

**UC5: User would like to discover the remoteID for the drone nearby them**
- Connection: BR1
- Actors: Users
- Flow:
  1.	User opens device.
  2.	User clicks on app.
  3.	User enters their username/email.
  4.	User enters their password.
  5.	User then hits sign in.
  6.	User is then directed to the screen consisting of drone flight paths in their immediate location and the drone list based on RemoteID.
  7.	The drone closest to the user will be listed at the top of the list of drone RemoteID’s.
- Explanation: A user may be curious about a drone’s RemoteID if the drone flight path may be suspicious or may be acting abnormally. This will allow law enforcement quick access to the drone information for a possible investigation if needed.

**UC6:User would like to monitor a drone flight**
- Connection: BR1
- Actors: Users
- Flow:
  1.	User opens device.
  2.	User clicks on app.
  3.	User enters their username/email.
  4.	User enters their password.
  5.	User then hits sign in.
  6.	User is then directed to the screen consisting of drone flight paths in their immediate location and the drone list based on RemoteID.
  7.	The drone closest to the user will be listed at the top of the list of drone RemoteID’s.
  8.	The user can hit the INFO button to see that specific drone flight path that will continuously update in real time.
- Explanation: A user may be suspicious about how a drone may be flying or acting in real time either based in person or the app. They would be able to monitor the drone flight in real time from the screen of their device because the app will update in real time.

**UC7:User would like to see specific drone data**
- Connection: BR2
- Actors: Users
- Flow:
  1.	User opens device.
  2.	User clicks on app.
  3.	User enters their username/email.
  4.	User enters their password.
  5.	User then hits sign in.
  6.	User is then directed to the screen consisting of drone flight paths in their immediate location and the drone list based on RemoteID.
  7.	User hits the INFO button beside the RemoteID they would like to look at.
  8.	The user is then directed to a screen consisting of information about the drone such as longitude, latitude, average speed, connection, description, etc.
- Explanation: A user having the ability to look at drone information will give them the ability to find information they are looking for quicker or provide information they may be curious about. The drone data will include the drone longitude, latitude, flight path, average speed, connection, description, operator name, approximate operator location based on initial flight, serial number. This is information that may be needed by law enforcement agencies.

**UC8:User would like to see specifc drone flight**
- Connection: BR2
- Actors: Users
- Flow:
  1.	User opens device.
  2.	User clicks on app.
  3.	User enters their username/email.
  4.	User enters their password.
  5.	User then hits sign in.
  6.	The user is then directed to the screen consisting of drone flight paths.
  7.	User hits the INFO button beside the drone RemoteID where they are then directed to a screen with the specific drone flight path and current location.
- Explanation: A user may wish to see the flight path for a specific drone rather than all drones in their immediate area. This information may be wanted out of curiosity or in the aspect of law enforcement trying to locate the operator or possibly investigating suspicious data. This feature will also allow the user to locate the current location of the drone.

**UC9: User would like to go back to the screen consisting of the flight paths of all drones and their remote IDs from a specific drone data information screen**
- Connection: BR2
- Actors: Users
- Flow:
  1.	User can see a specific drones information on their current screen consisting of the drones flight path, description, longitude, latitude, connection, serial number, etc.
  2.	User can then scroll to the bottom of the screen consisting of the data
  3.	User can then hit the back button at the bottom left of the screen.
  4.	User is then redirected back to the screen consisting of all drone flight paths and remoteID.
- Explanation: The user may have acquired all the information they may have wanted to access from the drone and now would like to see all the current drones in their immediate location as well as the remote ID’s. Being able to go back to the screen consisting of this information will allow for a more convenient access of information rather than having to close the app and sign in again.
