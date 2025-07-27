# 🪚 CNC Router Furniture Design Marketplace — Terminal Documentation

## 🎯 Project Overview and Vision

Vision:
  - A platform connecting CNC furniture designers with buyers and CNC machine owners.
  - Enable high-quality design transactions and real-world job collaborations.

Mission:
  - Marketplace for buying/selling CNC-ready design files.
  - Paid job ads for physical hiring.
  - Buyer requests with automatic file match resolution.
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
  - Image upload + notes
  - Designers auto-notified if they have a 100% match
  - Resolved automatically
  - Expired requests shown

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
  - reference image, notes
  - auto-matching system
  - resolved/expired flags

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
  - POST /requests/:id/resolve

Job Posts:
  - POST /jobs
  - GET /jobs
  - DELETE /jobs/:id

--------------------------------------------------------

## 🚀 Roadmap Summary

Phase 1 (MVP):
  - Auth, basic gig system, buyer purchase
  - Admin panel, payment

Phase 2:
  - Buyer requests + match
  - Designer dashboard, verification
  - Paid job posts

Phase 3:
  - Ranking system, featured listings
  - Messaging system

--------------------------------------------------------

## 🛡️ Legal Notes

- Digital downloads only (no physical delivery)
- Designers must own uploaded files
- USD only — no in-app currency
- No restriction on location or contact sharing

--------------------------------------------------------

# 📦 Done!
This terminal version includes all key points for the CNC Design Marketplace.

You can:
- Export this as `.txt` or `.md`
- Use it in README.md or CLI tools
- Ask for each schema or route individually in terminal-style files

