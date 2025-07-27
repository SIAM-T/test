# 🪚 CNC Router Furniture Design Marketplace — Terminal Documentation

## 🎯 Project Overview and Vision

Vision:
  - A platform connecting CNC furniture designers with buyers and CNC machine owners.
  - Enable high-quality design transactions and real-world job collaborations.

Mission:
  - Marketplace for buying/selling CNC-ready design files.
  - Paid job ads for physical hiring.
  - Buyer requests fulfilled through direct seller collaboration.
  - Paid verification and ranking system for designers.

Core Values:
  - File accuracy & design quality
  - Trusted collaboration
  - Transparent monetization
  - Professional empowerment
  - Seamless digital UX

--------------------------------------------------------

## 👤 User Types

1. Designers (Sellers)
   - Sell downloadable CNC design files
   - Post paid job ads
   - Get ranked, reviewed, and verified

2. CNC Owners (Buyers + Job Creators)
   - Buy designs for their machines
   - Post paid job listings to hire designers

3. General Buyers
   - Purchase designs
   - Submit custom requests with sample/reference images

--------------------------------------------------------

## 🔧 Key Platform Features

✅ Paid Verification System:
  - Monthly badge (no ID required)
  - Cancel anytime

🎨 Design Listing:
  - Upload files: .SVG, .DXF, .EPS, .AI, .PDF
  - Tagged: type, machine, size, complexity
  - Preview before download

🔍 Buyer Request System:
  - Buyers submit request with reference image & notes
  - Designers manually browse and contact buyers
  - Manual collaboration: Designer delivers custom-matching design
  - No auto file matching system
  - Requests expire after set time (e.g., 30 days)
  - Expired requests shown (for analytics or insights)

📢 Job Ads:
  - Paid by designers or CNC owners
  - Optional location filter
  - Fixed duration (e.g., 30 days)

🏅 Designer Ranks & Badges:
  - Auto-ranked by reviews/downloads
  - Badge for verified & top designers

--------------------------------------------------------

## 🔐 User Roles

Admin:
  - Manage designs, users, payments, disputes, job posts
  - View analytics

Designer:
  - Sell design files
  - Post job ads
  - View analytics, rank, badges

Buyer:
  - Purchase files
  - Post buyer requests
  - Collaborate with designers for custom design
  - View/download order files

--------------------------------------------------------

## 💰 Monetization Plan

- 5% commission on each sale
- Stripe processing fee (3%)
- Paid Verification Badge: $9.99/month
- Paid Job Posts: $4.99 for 30 days
- Optional: Featured Listings

--------------------------------------------------------

## 🧱 Tech Stack Summary

Frontend:
  - React + Next.js
  - Tailwind CSS, Framer Motion
  - Redux Toolkit + React Query

Backend:
  - Node.js + Express
  - MongoDB Atlas, Multer
  - Stripe (USD only)
  - AWS S3 for files

--------------------------------------------------------

## 🗃️ MongoDB Collections

users:
  - role: ['designer', 'buyer', 'admin']
  - isVerified, avatar, subscription
  - designerStats: downloads, rating, rank

designs:
  - title, category, tags
  - file: S3 URL
  - stats: downloads, views, rating

orders:
  - designId, buyerId, designerId
  - stripePaymentId, download link
  - timestamps, price breakdown

buyerRequests:
  - imageUpload, referenceNotes
  - postedBy: buyer
  - isExpired, isResolved
  - manually resolved through direct contact

jobPosts:
  - postedBy: designer or CNC owner
  - title, description, location
  - isPaid, expiresAt

--------------------------------------------------------

## 🔗 API Routes (REST)

Auth:
  - POST /auth/register
  - POST /auth/login
  - POST /auth/verify-payment

Designs:
  - GET /designs
  - POST /designs (Designer only)
  - GET /designs/:id
  - POST /designs/:id/purchase

Orders:
  - GET /orders (My orders)
  - GET /orders/:id

Buyer Requests:
  - POST /requests
  - GET /requests
  - PATCH /requests/:id/resolve (manually marked)
  - DELETE /requests/:id (admin/mod)

Job Posts:
  - POST /jobs
  - GET /jobs
  - DELETE /jobs/:id

--------------------------------------------------------

## 🚀 Roadmap Summary

Phase 1 (MVP):
  - Auth, design upload, design browsing & purchase
  - Admin panel, payment integration

Phase 2:
  - Buyer request system (manual match)
  - Job ads for hiring
  - Designer dashboard, verification

Phase 3:
  - Rankings, badges, featured listings
  - Internal messaging & notifications

--------------------------------------------------------

## 🛡️ Legal Notes

- Digital downloads only (no physical delivery by platform)
- Designers must own rights to all uploaded files
- USD only — no in-app tokens or coins
- No restrictions on global access or contact sharing
- No auto file matching; buyer-designer collaboration required

--------------------------------------------------------

# ✅ All Set!
This terminal-friendly documentation reflects your updated marketplace logic.
Let me know if you want this exported as `.txt`, `.md`, `.pdf`, or built into a CLI or onboarding guide.
