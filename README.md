# Project Documentation

### Goal for the The Project

1. Implement infinite scrolling for the calendar component by converting the `useRoomRateAvailabilityCalendar` query to use infinite queries with a cursor query parameter.
2. Optimize the horizontal scroll behavior of the calendar to ensure smooth and responsive scrolling.
3. Update the project documentation to reflect the changes made.

## Instructions for Check Code

1. **Setup the Project:**

   - Clone the repository from the provided URL.
   ```json
   git clone <repository-url>
   cd <project-directory>
   ```
   - Install the necessary dependencies using `npm install`.
   - Set up the environment variable `NEXT_PUBLIC_BACKEND_URL` with the base URL `https://beta.api.bytebeds.com`. Create .env file in your project root.

2. **Run the project:**

```json
npm start
```

3. **Implement Infinite Scrolling:**

   - Locate the `useRoomRateAvailabilityCalendar` query in the codebase.
   - Convert the query to use infinite queries. Use a `cursor` query parameter to fetch additional data when needed.
   - Ensure the calendar component can load more data\*\* as the user scrolls vertically.

4. **Optimize Scroll Behavior:**

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
