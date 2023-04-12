# Technical Specification for Anime Illustrator E-commerce Website

## Technology Stack

**Frontend:** Next.js (React) with TypeScript and Tailwind CSS

**Backend:** Node.js with Express

**Database:** MongoDB

**Authentication:** Firebase Authentication

**Image Storage:** Cloudinary

**Payment Gateway:** Stripe

## Features

- User authentication (login, registration, password reset)
- Browse and search for illustrations
- Detailed illustration pages
- Shopping cart and checkout
- Secure payment processing
- User profile and order history
- Admin panel for managing illustrations and orders

## File Structure

```
├── components/
│   ├── Layout/
│   │   ├── HamburgerMenu.tsx
│   │   └── Layout.tsx
│   ├── HeroImage/
│   │   ├── HeroImage.tsx
│   │   └── HeroImageCarousel.tsx
│   ├── Illustration/
│   │   ├── IllustrationCard.tsx
│   │   └── IllustrationList.tsx
│   ├── ShoppingCart/
│   │   ├── CartItem.tsx
│   │   └── ShoppingCart.tsx
│   ├── User/
│   │   ├── LoginForm.tsx
│   │   ├── RegisterForm.tsx
│   │   └── UserProfile.tsx
│   └── SocialMediaFeeds/
│       ├── InstagramFeed.tsx
│       ├── TwitterFeed.tsx
│       └── YouTubeFeed.tsx
│
├── pages/
│   ├── index.tsx
│   ├── illustrations.tsx
│   ├── illustration/[id].tsx
│   ├── cart.tsx
│   ├── profile.tsx
│   ├── admin.tsx
│   ├── login.tsx
│   ├── register.tsx
│   ├── forgot-password.tsx
│   └── reset-password.tsx
│
├── public/
│   └── images/
│
├── services/
│   ├── api.ts
│   ├── auth.ts
│   ├── illustrations.ts
│   ├── orders.ts
│   └── socialMedia.ts
│
├── styles/
│   └── tailwind.config.js
│
├── utils/
│   ├── types.ts
│   └── utils.ts
│
├── .env
├── .gitignore
├── next.config.js
├── package.json
├── README.md
└── tsconfig.json

```

## User Interface

- Landing page (home) with:
  - Hamburger menu for navigation
  - Hero image with automatic image rotation
  - Featured illustrations and search functionality
  - Embedded Twitter, Instagram, and YouTube feeds
- Illustration browsing with filtering and sorting
- Detailed illustration page with description, price, and add-to-cart functionality
- Shopping cart and checkout flow
- User profile and order history page
- Admin panel for managing illustrations and orders
- Login, registration, and password reset pages

## Database Schema

**User**

- ID
- Email
- Name
- Role (customer, admin)
- Created At
- Updated At

**Illustration**

- ID
- Title
- Description
- Price
- Image URL
- Thumbnail URL
- Tags (array of strings)
- Created At
- Updated At

**Order**

- ID
- User ID (foreign key)
- Illustration ID (foreign key)
- Quantity
- Total Price
- Shipping Address
- Billing Address
- Payment Status
- Created At
- Updated At

## API Endpoints

**Auth**

- POST /auth/register
- POST /auth/login
- POST /auth/forgot-password
- POST /auth/reset-password

**Illustrations**

- GET /illustrations
- GET /illustrations/:id
- POST /illustrations (admin only)
- PUT /illustrations/:id (admin only)
- DELETE /illustrations/:id (admin only)

**Orders**

- GET /orders (user or admin)
- GET /orders/:id (user or admin)
- POST /orders
- PUT /orders/:id (admin only)
- DELETE /orders/:id (admin only)

## Third-Party Services

- Firebase Authentication for user authentication
- Cloudinary for image storage and resizing
- Stripe for payment processing
- SendGrid for transactional emails (password reset, order confirmation)

## Testing

- Unit tests with Jest and React Testing Library for frontend components
- Integration tests with Supertest for backend API endpoints

## Deployment

- Frontend and backend deployed on Vercel
- MongoDB hosted on MongoDB Atlas

```

```
