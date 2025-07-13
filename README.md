# 🎬 JustTix Movie Ticket Booking Website (MERN)

Movie Ticket Booking Website built using the **MERN Stack** (MongoDB, Express, React, Node.js), with modern authentication via **Clerk**, background jobs via **Inngest**, and real-time movie data fetched from the **TMDB API**.
Users can explore movies, choose seats, and book tickets. Admins can manage movies and bookings via a dashboard.


---

##  Features

### User Features
-  Authentication via Clerk (Email + Password, Email OTP, Google OAuth)
-  Browse movie listings
-  Browse real-time movie data from [TMDB](https://www.themoviedb.org/)
-  Select seats while booking
-  Receive booking confirmations and reminders via email

###  Admin Features
-  Add or remove movies
-  View all bookings in the dashboard

###  Background Jobs via Inngest
-  Send email to all users when a new movie is added
-  Booking confirmation email
-  Reminder email sent before the movie starts
-  Auto-release seats if confirmation is not completed within 10 minutes.

---


##  Tech Stack

| Layer       | Tech                            |
|-------------|----------------------------------|
| Frontend    | React.js, Tailwind CSS           |
| Backend     | Node.js, Express.js, MongoDB     |
| Auth        | [Clerk](https://clerk.dev)       |
| Background Jobs | [Inngest](https://www.inngest.com) |
| Email       | [Resend](https://www.npmjs.com/package/resend)


---

## Inngest + Clerk User Sync

We also use **Inngest** to automatically sync user data from Clerk to our MongoDB database.


##  Screenshots
**Login page**
<img width="1916" height="893" alt="Image" src="https://github.com/user-attachments/assets/7249f189-2bb2-40fb-8cb5-117a7faa803b" />

**Home page**
<img width="1919" height="952" alt="Image" src="https://github.com/user-attachments/assets/068a7fc6-db6d-4223-adfc-f2fb6d4382e9" />

**Upcoming movie page**
<img width="1918" height="909" alt="Image" src="https://github.com/user-attachments/assets/22cfe88d-99a1-4609-93d1-b2124db61a75" />

**Movie description page**
<img width="1919" height="946" alt="Image" src="https://github.com/user-attachments/assets/73a029a7-b711-4481-ae48-34078f178f48" />

**Booking page**
<img width="1919" height="939" alt="Image" src="https://github.com/user-attachments/assets/571f9afa-9551-4a06-af70-139f85ac1cd4" />

---
**Admin page**
<img width="1917" height="945" alt="Image" src="https://github.com/user-attachments/assets/8707d4b3-0d1a-4f3b-9ae4-77da468ac53a" />


## Challenges Faced

- **TMDB API Access Issue**: The TMDB API wasn’t working locally due to regional restrictions—we had to use a VPN to access it.
   Later, we realized the API worked fine in production, so we deployed the project on Vercel to test and confirm successful data fetching.

- **Seat Reservation & Auto-Release**: When a user selects seats, we temporarily lock them for 10 minutes to
  prevent others from booking the same ones. If the user doesn’t confirm the booking within that time, the seats
 are automatically released using a background job powered by Inngest.



# Contributors

<table> <tr> <td align="center"> <a href="https://github.com/sakshiji-here"> 
  <img src="https://avatars.githubusercontent.com/sakshiji-here" width="75px;" alt="Sakshi"/> <br /> 
  <sub><b>Sakshi Singh</b></sub> </a> <br /> Frontend UI </td> <td align="center"> <a href="https://github.com/iamkrvishal07"> 
  <img src="https://avatars.githubusercontent.com/iamkrvishal07" width="75px;" alt="Vishal Kumar"/> <br /> <sub><b>Vishal Kumar</b></sub> </a>
<br />Backend </td> </tr> </table>






