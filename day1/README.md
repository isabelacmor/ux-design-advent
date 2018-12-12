### Challenge
The NYC metrocard system has remained unchanged for decades. The cost of the metrocard machine infrastructure, the lost time of waiting in line to buy a metrocard, touching a dirty machine to do it, the potential of losing the metrocard, and the ease of gaming the system by swiping your card for others has cost the city millions of dollars and leaves much to be desired from the user experience.

Design a new system that allows a daily user who uses the metro everyday or an-out-of-town visitor who will use the metro just once to get access to the metro, on time, without having a physical NYC metrocard on hand.

-------
### Defining the problem
1. Problems we're trying to address
    - Cost of physical ticket machines
    - Time consuming to buy tickets
    - Losing tickets
    - Pass-backs
2. Target audience
    - Daily users
    - One-off users

### Personas
- Primary Personas
    1. Daily commuter
        - Key characteristics
            - Confident using the rail system and their current commuter card
            - Usually has their commuter card handy, but misplacing it would be a big setback
            - Uses the rail 4+ times per week
        - Motivations
            - Wants to ensure they get to work on time every day without missing the rail
            - One less thing to worry about having on them / one less thing to misplace
    2. Tourists
        - Key characteristics
            - Not confident using the rail system or familiar with the current route options and ticketing systems
            - Doesn't have a commuter card
            - Will use the rail a few times and then likely will never use it again
        - Motivations
            - Easy to obtain a ticket and reload on demand
            - Prefers to not need to understand the local language or need local currency if applicable
            - Find the right route and easily buy a ticket for that route
- Secondary personas
    1. Infrequent commuters
        - Key characteristics
            - Knows their way around the rail system
            - More likely to forget to bring their commuter card with them when they want to ride the rail
            - Uses the rail 1-2 times per week
        - Motivations
            - Easy to reload a card on demand when they feel like taking the rail
            - Find the right route / schedule for their trip
    2. Low-income commuters
        - Key characteristics
            - More likely to not have technology available for a "smart" card solution
            - More likely to use discounted fares
        - Motivations
            - Getting a commuter card is low-barrier to entry and can be done and maintained without any special equipment

### Initial thoughts
- A physical card-based system with a supporting app / website to refill cards. The problem with that is that you would still have issues with losing tickets and with one-off users who would need to obtain a physical card before being able to use the transit system.
- A mobile app with a QR code seems like a good first step. It eliminates the need for a physical ticket and users would likely have a mobile phone easily accessible to display the QR code to the scanner. The app would also eliminate the need for physical ticket machines and the lost time in line, since users would be able to add funds to their e-ticket through the app.

    In addition, it still provides users with the same opportunity to use a physical ticket if they'd prefer by printing out their QR code. This could go as far as having the QR code laminated and put on a keyring.

    This solution wouldn't address the pass-back issue, although it is something that could be solved in parallel by implementing software that detectsp pass-backs by detecting that the QR code has already been scanned within the last N minutes. Alternatively, as other cities such as Seattle have already implemented for unmanned transit, a pass-back swipe cancels out the original swipe.

    This solution might also be more difficult to implement for the low-income commuter, although they could do a one-time setup at an automatic machine at a rail station or on the website at home / school / the local library. Machines could still be available at rail stations where the QR code could be scanned and money / credit cards used to deposit funds. QR codes could also be looked up via a name / birthday / pin combination in case they need to be reprinted.

### Competitive Analysis
1. #### [Athens Transit System](https://www.athenstransport.com/english/tickets/)
    - Paper and plastic smartcards
    - Can be bought from and recharged at all transit ticket offices and automatic ticket issuing machines
    - Rechargeable
    - Personalized option available, with name, photo, and option to recharge via app or NFC instead of just at the ticket machines
2. #### [MTA eTix](http://www.mta.info/mta-eTix-promo)
    - App that allows for mobile ticketing via QR code and buying tickets via a credit card or debit card
    - App also gives additional information about rail time tables, stations, advisory alerts, etc.

### Proposed solution
#### Mobile app with QR code + physical ticket station
App features:
- Create an account which is accessed with your last name and pin
- Generate a unique QR code that serves as your permanent ticket
- Add funds to your ticket
- Suspend your QR code and regenerate (for lost / stolen QR codes)
- Printable QR code for lamination / keychain / etc. Can be decided by the user for increased personalization
- Time tables and schedules
- Route / trip planning, including cost estimations

Ticket station features: 
- All the same features as the app, but in a physical ticket station at each rail stop for commuters who may not have access to the technology required for the app

### User Flow
<img width="742" alt="capture2" src="https://user-images.githubusercontent.com/4714094/49852097-0117e680-fd98-11e8-8ded-76e821229415.PNG">