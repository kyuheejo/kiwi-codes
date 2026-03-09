# Ridesharing App (Split.it)

Description: Cost Pooling for Ride-share Apps
Status: Shipped
Tags: Social
Role: Fullstack developer
When: January 15, 2022

![image.png](Ridesharing%20App%20(Split%20it)/image.png)

## TL;DR

Split.it is platform that allows JHU students who use ride-sharing apps to easily find people to split the fare with. The app was designed to leverage the social trust present in the Hopkins community to make organizing cheap transportation simple. I worked with a team of 6 SWEs, and was responsible for all of the UI/UX design, frontend development as well as the backend for the fully-integrated chat. Check out our project [here](https://www.trysplit.it/)!

## Problem Statement

College students love saving money and Hopkins students are no exception.  One of the problems that Hopkins students face is paying an egregious amount of money for ride sharing apps due to the difficulties of finding people to share a ride with.  JHU students already try to post on GroupMe to find other students to split costs, but this solution is difficult to manage and reaches only a small portion of the overall JHU population.

## Proposed Solution

Our platform allows Hopkins students who use ride-sharing apps to easily find people to split the fare with. The app will leverage the social trust present in the Hopkins community to make organizing cheap transportation simple.

Our application will be a progressive web application, which is both a downloadable mobile application and accessible on desktop. The application will have two main views – a calendar view, where events are displayed on a calendar based on date and time, and a card view, which is more conducive to searching and scrolling.

Users will be able to create two main types of events. One type of event is scheduled, which will show up on both the card view and the calendar view. This event has a set date, start and end location, and time. The other type of event is an unscheduled event, which is more to judge interest based on other users’ availability. This type of event will only show up on the card view, and will possibly have a polling feature.

Users will be able to register for the application with their jh.edu emails, ensuring that all users of the application will be Hopkins students or faculty. Users will be allowed to display certain amounts of information, including their major/department and year, and could be pseudo-anonymous if desired. Users could potentially link their venmo to their account as well.

To facilitate communication, there will be a chat function where people who have committed to an event can all join one group chat. Users would be encouraged to plan either on the application or exchange phone numbers for easier access to information. To ensure that users can find each other, there will be some form of verification that will link all group members together.

## Potential Clients

- JHU students that regularly use ride-sharing apps
    - Riding to airport
    - Riding to entertainment venues
    - Going grocery shopping (Hmart, Great Wall Supermarket, Giant, etc.)
- JHU students with a car
    - Wanting to split gas costs to far destinations
    - Find it difficult to find parking within a destination but can’t justify the cost w/o other people.
- We could expand our potential clients to other campuses or organizations in the future

## Functional Requirements

### Core requirements

- JHU authentication
- Login
- Communal calendar
- Card display
- Create a ride share event
    - For one time
    - For many possible times
- Joining an existing event
- Filter by time, location, etc.
- View all existing events on a calendar
- Internal messaging

### Non-functional Requirements

- Secure storage of private user data, transmission of data
- Anonymous communication between users
- Easy to use and free of charge
- Responsive and polished UI/UX
- Works across platforms

## User Stories

## Must-Have

- As a user, I would like to have a calendar view to easily see how trips fit into my schedule.
- As a user, I want to be able to post my trip event on a shared calendar that contains time and location information. (specified by start location, time, end location)
- As a user, I would like to have a list **view of cards** to see unscheduled/unplanned trips that other people post. i.e As a user, I want to browse current postings.
- As a user, I want to find other people who are looking to book a rideshare to the same destination around a similar time as I am so I can easily find a ride that matches my schedule.
- As a user, I want to send a chat message to the people who have committed to my ride so I can coordinate the meet up.
- As a user, I want to be able to sign in using my **JHU credentials** to ensure everyone using the platform is a Hopkins student.
- As a user, I want to drop an event in case a conflict occurs so that I can give up my position to other users.
- As a user, I want to be able to filter events by location and time to more easily find trips that I would be interested in.
- As a user, I want to **search** for trips using keywords to more easily find my best trip.

## Nice-to-Have

- As a user, I want to see a reliability score associated with other users so that I have a way to trust other users will share the cost with me and feel comfortable connecting with them.
- As a user, I would like to give feedback on my copassengers to warn others of them or commend them.
- As a user, I would like to keep my identity anonymous within a platform so I can feel safe interacting with other people within the app.
- As a user, I want to create a user profile to add more customization and personalization to the application.
- As a user, I want to be able to have a form of verification so that I can guarantee that I am riding with the correct people.
- As a user, I would like to be notified when another user is interested in my posting so I don’t have to check for updates.
- As a user, I want to receive push notifications so I can be reminded of my trips and other various events (canceling trips).
- As a user, I would like to be able to see if I’ve ridden with another user before to ensure the most convenience.
- As a user, I would like to schedule an event with several potential times instead of creating many events to not create clutter in the calendar.
- As a user, I would like to be able to close an event when it reaches the desired number of riders so no one tries to join over the cap.
- As a user, I would like to be notified when other people drop an event that I have joined so other people may fill the spot.
- As a user, I want to be able to receive confirmations in my JHU email for my own ease of access to information.
- **As a user, I want to see how many people have registered for a certain event so I can have more information about trips.**
- As a user, I want to sort events by **proximity of its start location** to my current location to more easily find my best trip.
- As a user, I want to filter trips by tags / types to more easily find my best trip.
- As a user, I want to create a group chat among the people who have committed to the same ride so we can coordinate a meetup.
- As a user, if an event is full, I would like an option to copy the event so I can create a new event for other people who might also be interested.
- As a user, I want to be able to join a waitlist for an event if it is currently full so I can get a ride with the most optimal time and location for myself.
- As a user, I would like to schedule an event with several potential times instead of creating many events.
- As a user, I would like to receive poll results on the most favored time to go on a trip based on the potential listed times so I can choose the time with the most interest.
- As a user, I want events that are identical to be merged or split based on interest so I can always be able to find a group to ride with.

# Roadmap

### Iteration-1 : “CRUD Iteration”

// Focus on create events & displaying events

// Event generating user functionality

1. As a user, I want to be able to post my trip event on a shared calendar that contains time and location information. (specified by start location, date/time, end location)
2. As a user, I would like to have a **calendar view** to easily see how trips fit into my schedule.
3. As a user, I would like to have a list **view of cards** to see unscheduled/unplanned trips that other people post. i.e As a user, I want to browse current postings.
4. As a user, I want to be able to filter events by location and time to more easily find trips that I would be interested in.
5. As a user, I want to **search** for trips using keywords to more easily find my best trip.
    
    ![Screen Shot 2025-01-15 at 10.49.43 PM.png](Ridesharing%20App%20(Split%20it)/Screen_Shot_2025-01-15_at_10.49.43_PM.png)
    

### Iteration-2 : “Sign-in Iteration”

1. As a user, I want to be able to sign in using my **JHU credentials** to ensure everyone using the platform is a Hopkins student.
2. As a user, I want to **add and also drop** an event in case a conflict occurs so that I can give up my position to other users.
3. As a user, I want to be able to receive confirmations in my JHU email for my own ease of access to information.
4. As an event owner, I wanted to be **notified** when other people register to my event so I don’t have to check for updates.
5. As a user, I want to see how many people have registered for a certain event so I can have more information about trips.
6. As a user, I want to create a user profile to add more customization and personalization to the application.

### Iteration-3 : “User Functionality Iteration”

1. As a user, I want to be able to view contact information (phone number) for students on my trip so that I can coordinate the ride.
2. As a user, I want to be able to set the capacity when creating an event.
3. As an owner, I want to be able to edit the logistics of my event before the change deadline.
    1. As a participant of a recently edited ride, I want to be notified of the changes.
4. As a user, I want to be able to filter by all of my personal events.
5. As a tester, I want to be able to login through a backdoor without needing SSO.
6. As a user, I don’t want to be demoralized seeing full or old events that I cannot join no matter how much I would like to.
7. As a user, I want to have more JHU locations prefilled.
8. As a user, I want to use an alias/nickname for locations

### Iteration-4 : “User Experience Iteration”

1. As a user, I want to send a chat message to the people who have committed to my ride so I can coordinate the meet up.
2. As a user, I want to create a group chat among the people who have committed to the same ride so we can coordinate a meetup.
3. As a user, I would like to be able to see if I’ve ridden with another user before to ensure the most convenience.
4. As a user, I want to create a roundtrip event

### Iteration-5 : “Final Features Iteration”

1. As a user, I would like to schedule an event with several potential times instead of creating many events.
2. As a user, I want to be able to have a form of verification so that I can guarantee that I am riding with the correct people.
3. As a user, I want events that are identical to be merged or split based on interest so I can always be able to find a group to ride with.
4. As a user, if an event is full, I would like an option to copy the event so I can create a new event for other people who might also be interested.
5. As a user, I want to be able to join a waitlist for an event if it is currently full so I can get a ride with the most optimal time and location for myself.
6. As a user, I want to sort events by **proximity of its start location** to my current location to more easily find my best trip.
7. As a user, I want to filter trips by tags / types to more easily find my best trip.
8. As a user, I want to see a reliability score associated with other users so that I have a way to trust other users will share the cost with me and feel comfortable connecting with them.
9. As a user, I would like to give feedback on my copassengers to warn others of them or commend them.

### Iteration-6 : “Polishing Iteration”

1. As a user, I would like to have a bug-free and well-developed application.