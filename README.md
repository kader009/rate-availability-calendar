# Project Documentation

## Overview

Grit System Technical Assessment for Front-End Engineers.

### Goal for the The Project

1. Implement infinite scrolling for the calendar component by converting the `useRoomRateAvailabilityCalendar` query to use infinite queries with a cursor query parameter.
2. Optimize the horizontal scroll behavior of the calendar to ensure smooth and responsive scrolling.
3. Update the project documentation to reflect the changes made.

## Rate Calendar API Documentation

### Base URL

`https://beta.api.bytebeds.com`

### Endpoint

`GET /api/v1/property/{property_id}/rate-calendar/assessment`

### Query Parameters

- `property_id` (number): The ID of the property.
- `start_date` (string): The start date for the calendar data in YYYY-MM-DD format.
- `end_date` (string): The end date for the calendar data in YYYY-MM-DD format.
- `cursor` (number, optional): The cursor for pagination, used for infinite scrolling.

### Response

The response contains the following structure:

```json
{
  "room_categories": [
    {
      "id": "string",
      "name": "string",
      "occupancy": "number",
      "inventory_calendar": [
        {
          "id": "string",
          "date": "string",
          "available": "number",
          "status": "boolean",
          "booked": "number"
        }
      ],
      "rate_plans": [
        {
          "id": "number",
          "name": "string",
          "calendar": [
            {
              "id": "string",
              "date": "string",
              "rate": "number",
              "min_length_of_stay": "number",
              "reservation_deadline": "number"
            }
          ]
        }
      ]
    }
  ],
  "nextCursor": "number"
}
```

## Instructions for Check Code

1. **Setup the Project:**

   - Clone the repository from the provided URL.
   - Install the necessary dependencies using `npm install`.
   - Set up the environment variable `NEXT_PUBLIC_BACKEND_URL` with the base URL `https://beta.api.bytebeds.com`.
   - Than follow the step `npm start`.

2. **Implement Infinite Scrolling:**

   - Locate the `useRoomRateAvailabilityCalendar` query in the codebase.
   - Convert the query to use infinite queries. Use a `cursor` query parameter to fetch additional data when needed.
   - Ensure the calendar component can load more data\*\* as the user scrolls vertically.

3. **Optimize Scroll Behavior:**

   - Analyze the current implementation of the calendar's horizontal scroll behavior.
   - Identify the causes of the laggy scroll performance.
   - Optimize the scroll behavior to ensure it is smooth and responsive.

### File(s) Modified:

- `useRoomRateAvailabilityCalendar.tsx` – Updated to implement infinite scrolling with a `cursor` query parameter.
- `page.tsx` – Integrated the infinite query with the page component to handle data loading on scroll.
- `global.css` – Updated styling for scroll behavior and added smooth transitions.
- `roomcalendar.tsx` – Enhanced the calendar component to handle infinite data loading and updated rendering logic for smooth scrolling.

### Summary of Changes:

- Applied performance optimizations to improve the smoothness of the calendar's horizontal scrolling.
- Updated CSS for better rendering and user experience during scroll events.
