# Runa Backend

Backend API for Runa, a short-distance delivery platform that matches senders with nearby drivers within a 5-mile radius. It handles bookings, pricing, payments, job dispatch, driver earnings, and the partner integration with Ovaboss.

## Status

Early development (MVP). Stack and framework decisions are still open, marked **TBD** below.

## Features

- Sender bookings with a 5-mile radius check on pickup and drop-off
- Distance-based pricing from admin-configured per-mile rates
- Payments through Paystack and Flutterwave (sandbox first)
- Job broadcast to nearby online drivers, with locking so only one driver can accept a job
- Job status tracking: Created, Paid, Broadcast, Accepted, Arriving, Picked up, In transit, Delivered, Cancelled, Expired
- Proof of delivery with a hashed, attempt-limited, expiring 4-digit OTP
- Append-only driver wallet ledger with per-trip earnings, incentive bonuses, and withdrawal requests
- Partner API (`POST /partner/orders`) for Ovaboss orders, with API key auth and idempotency keys
- Admin endpoints for driver approval, pricing, incentives, and live job monitoring
