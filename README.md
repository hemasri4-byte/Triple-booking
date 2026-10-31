# Triple-booking
# Triply — Bus & Train Booking Demo

A responsive travel booking demo built with React, Vite, Express, and Lucide icons.

## Requirements
- Node.js 18+ (Node.js 20+ recommended)
- npm

## Run locally

1. Extract the ZIP and open a terminal in the `triply-booking` directory.
2. Install packages:

   ```bash
   npm install
   ```

3. Start the frontend and backend together:

   ```bash
   npm run dev
   ```

4. Open the Vite URL shown in the terminal, usually `http://localhost:5173`.

The Express API runs at `http://localhost:4000`. You can test it at `/api/health`.

## API endpoints

- `GET /api/health` — API health check
- `GET /api/services?mode=Train&source=Vijayawada&destination=Chennai&date=2026-11-05` — sample service list
- `POST /api/bookings` — validates and returns a demo booking reference

Example request body:

```json
{
  "mode": "Train",
  "source": "Vijayawada",
  "destination": "Chennai",
  "date": "2026-11-05",
  "serviceId": "train-12604",
  "seats": ["A2"],
  "passengers": [{"name": "Example Traveller", "age": "24", "gender": "Male"}],
  "contact": {"email": "traveller@example.com", "phone": "9876543210"}
}
```

## Important limitations

- Service names, schedules, fares, and seat maps are demonstration data.
- The booking endpoint creates a demo confirmation only. It does not reserve seats, issue real tickets, or charge money.
- Return-trip date selection is present in the UI, but the demo API does not perform a return-leg search.
- A production system needs an authorized bus/train inventory provider, server-side inventory locking, persistent database storage, authentication, payment integration, cancellation/refund handling, monitoring, and privacy/security review.
- Do not use the demo as a source of real travel information.
- 
