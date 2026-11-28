# Campus Venue Booking

A lightweight campus venue booking dashboard for Lovely Professional University. Students can browse venue facilities, check hourly availability, and submit booking requests, all in the browser with no installation, server, or build step.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## Features

- Browse four venues and view seating capacity, projector, microphone system, and air conditioning details.
- Check eight one-hour time slots per day, color-coded as **Available**, **Pending**, or **Reserved**.
- Submit a booking request with event details, expected attendance, and optional AV equipment.
- Built-in validation:
  - No bookings for past dates
  - No events above the venue's seating capacity
  - No double booking of a slot that is already pending or reserved
- Live summary counters for venues, total bookings, and pending requests.
- View booking status and cancel a booking to free its slot again.
- Bookings persist between visits using browser local storage.
- Responsive layout for desktop and mobile screens.

## Tech Stack

- **HTML5** for page structure and the booking form
- **CSS3** for responsive styling (flexbox and grid)
- **Vanilla JavaScript** for venue data, availability, validation, and local storage

## Getting Started

No installation or build step is needed.

1. Clone or download this repository.
2. Open `index.html` in any modern web browser.

Alternatively, serve the folder with any static file server and open the local URL it provides.

```bash
git clone <repository-url>
cd <project-folder>
# then open index.html in your browser
```

## How to Use

1. Select a venue in the directory to see its facilities.
2. In **Request a Booking**, choose a venue and a date.
3. Click an available time slot, then enter your name, event name, and expected attendance.
4. Tick any AV equipment you need.
5. Click **Send Booking Request**. It appears in the booking list with **Pending** status.
6. Use **Cancel** to remove a booking and make its slot available again.

Pending requests block the selected slot just like reserved bookings. The interface has no approval controls yet; `approveBooking(index)` exists in `script.js` for demo use from the browser console, for example `approveBooking(0)`.

## Venues and Time Slots

| Venue | Capacity | Projector | Mic System | AC |
|---|---|---|---|---|
| Auditorium | 500 | 4K Laser Projector | Wireless handheld + podium + lapel | Central AC |
| Mini Seminar Hall | 120 | Full HD Projector | 2 wireless handheld mics | Split AC |
| Smart Classroom | 60 | Interactive Smartboard | 1 collar mic | Split AC |
| Conference Room | 20 | Wall-mounted LED Display | Tabletop conference mic | Split AC |

Time slots run hourly from 09:00 to 17:00. Venues and slots are defined near the top of `script.js`, so they are easy to edit.

## Project Structure

```
.
├── index.html   # Page structure and booking form
├── style.css    # Responsive styling
├── script.js    # Venue data, availability, validation, local storage
└── README.md
```

## Data and Privacy

Bookings are saved under the `campusBookings2` key in the browser's `localStorage`. They stay on that browser profile unless browser storage is cleared. This demo has no server, account system, or shared database, so bookings are not shared with other users or devices.

## Limitations and Future Improvements

- Add
