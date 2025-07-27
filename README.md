REACT.JS FRONTEND FILE STRUCTURE
=====================================

frontend/
├── public/
│   ├── index.html                    # Main HTML template, contains root div and meta tags
│   ├── favicon.ico                   # Website favicon
│   ├── manifest.json                 # PWA manifest for mobile app-like experience
│   └── robots.txt                    # SEO robots configuration
│
├── src/
│   ├── index.js                      # Application entry point, renders App component into DOM
│   ├── App.js                        # Main app component, contains routing and global providers
│   ├── App.css                       # Global app styles and CSS variables
│   │
│   ├── components/                   # Reusable UI components
│   │   ├── common/                   # Generic reusable components
│   │   │   ├── Header/
│   │   │   │   ├── Header.js         # Main navigation header with user menu and logo
│   │   │   │   ├── Header.css        # Header-specific styles and responsive design
│   │   │   │   └── index.js          # Export barrel for Header component
│   │   │   │
│   │   │   ├── Footer/
│   │   │   │   ├── Footer.js         # Site footer with links, copyright, social media
│   │   │   │   ├── Footer.css        # Footer styling and layout
│   │   │   │   └── index.js          # Export barrel for Footer component
│   │   │   │
│   │   │   ├── Cards/
│   │   │   │   ├── ProductCard.js    # Displays product info with image, price, actions
│   │   │   │   ├── ServiceCard.js    # Shows service details with provider info
│   │   │   │   ├── ProfileCard.js    # User profile summary card component
│   │   │   │   ├── Cards.css         # Shared card styles and hover effects
│   │   │   │   └── index.js          # Exports all card components
│   │   │   │
│   │   │   ├── Forms/
│   │   │   │   ├── FormInput.js      # Reusable input component with validation
│   │   │   │   ├── FormSelect.js     # Dropdown select component with search
│   │   │   │   ├── FormTextarea.js   # Multi-line text input with character count
│   │   │   │   ├── FormButton.js     # Styled button with loading states
│   │   │   │   ├── FormCheckbox.js   # Checkbox input with custom styling
│   │   │   │   ├── Forms.css         # Form component styles and validation states
│   │   │   │   └── index.js          # Exports all form components
│   │   │   │
│   │   │   ├── Modals/
│   │   │   │   ├── Modal.js          # Base modal component with backdrop and animations
│   │   │   │   ├── ConfirmModal.js   # Confirmation dialog for destructive actions
│   │   │   │   ├── ImageModal.js     # Full-screen image viewer with zoom
│   │   │   │   ├── Modals.css        # Modal styling, animations, and responsive design
│   │   │   │   └── index.js          # Exports all modal components
│   │   │   │
│   │   │   ├── Layout/
│   │   │   │   ├── Container.js      # Responsive container with max-width constraints
│   │   │   │   ├── Grid.js           # Flexible grid system for layouts
│   │   │   │   ├── Sidebar.js        # Collapsible sidebar for navigation
│   │   │   │   ├── Layout.css        # Layout component styles and breakpoints
│   │   │   │   └── index.js          # Exports all layout components
│   │   │   │
│   │   │   └── Loading/
│   │   │       ├── Spinner.js        # Loading spinner component with size variants
│   │   │       ├── LoadingCard.js    # Skeleton loading card for content placeholders
│   │   │       ├── Loading.css       # Loading animation styles and keyframes
│   │   │       └── index.js          # Exports all loading components
│   │   │
│   │   ├── auth/                     # Authentication-related components
│   │   │   ├── LoginForm/
│   │   │   │   ├── LoginForm.js      # User login form with email/password validation
│   │   │   │   ├── LoginForm.css     # Login form specific styling
│   │   │   │   └── index.js          # Export barrel for LoginForm
│   │   │   │
│   │   │   ├── RegisterForm/
│   │   │   │   ├── RegisterForm.js   # User registration with form validation
│   │   │   │   ├── RegisterForm.css  # Registration form styling
│   │   │   │   └── index.js          # Export barrel for RegisterForm
│   │   │   │
│   │   │   ├── ForgotPassword/
│   │   │   │   ├── ForgotPassword.js # Password reset request form
│   │   │   │   ├── ForgotPassword.css# Forgot password form styling
│   │   │   │   └── index.js          # Export barrel for ForgotPassword
│   │   │   │
│   │   │   ├── ResetPassword/
│   │   │   │   ├── ResetPassword.js  # Password reset form with token validation
│   │   │   │   ├── ResetPassword.css # Reset password form styling
│   │   │   │   └── index.js          # Export barrel for ResetPassword
│   │   │   │
│   │   │   └── ProtectedRoute/
│   │   │       ├── ProtectedRoute.js # Route wrapper that requires authentication
│   │   │       └── index.js          # Export barrel for ProtectedRoute
│   │   │
│   │   ├── marketplace/              # Marketplace-specific components
│   │   │   ├── ProductGrid/
│   │   │   │   ├── ProductGrid.js    # Grid layout for displaying multiple products
│   │   │   │   ├── ProductGrid.css   # Product grid responsive styling
│   │   │   │   └── index.js          # Export barrel for ProductGrid
│   │   │   │
│   │   │   ├── ProductDetail/
│   │   │   │   ├── ProductDetail.js  # Detailed product view with images and description
│   │   │   │   ├── ProductDetail.css # Product detail page styling
│   │   │   │   └── index.js          # Export barrel for ProductDetail
│   │   │   │
│   │   │   ├── SearchFilters/
│   │   │   │   ├── SearchFilters.js  # Product search and filtering interface
│   │   │   │   ├── SearchFilters.css # Search filters styling and layout
│   │   │   │   └── index.js          # Export barrel for SearchFilters
│   │   │   │
│   │   │   ├── ShoppingCart/
│   │   │   │   ├── ShoppingCart.js   # Shopping cart component with item management
│   │   │   │   ├── CartItem.js       # Individual cart item with quantity controls
│   │   │   │   ├── ShoppingCart.css  # Shopping cart styling
│   │   │   │   └── index.js          # Export barrel for shopping cart components
│   │   │   │
│   │   │   └── Checkout/
│   │   │       ├── CheckoutForm.js   # Multi-step checkout process
│   │   │       ├── PaymentForm.js    # Payment information form
│   │   │       ├── AddressForm.js    # Shipping address form
│   │   │       ├── OrderSummary.js   # Order review and totals
│   │   │       ├── Checkout.css      # Checkout process styling
│   │   │       └── index.js          # Export barrel for checkout components
│   │   │
│   │   ├── designer/                 # Designer dashboard components
│   │   │   ├── DesignerProfile/
│   │   │   │   ├── DesignerProfile.js# Designer profile management and display
│   │   │   │   ├── PortfolioUpload.js# Portfolio image upload and management
│   │   │   │   ├── SkillsManager.js  # Skills and expertise management
│   │   │   │   ├── DesignerProfile.css# Designer profile styling
│   │   │   │   └── index.js          # Export barrel for designer profile components
│   │   │   │
│   │   │   ├── ProjectManager/
│   │   │   │   ├── ProjectList.js    # List of designer's active projects
│   │   │   │   ├── ProjectDetail.js  # Individual project management interface
│   │   │   │   ├── ProjectForm.js    # Create/edit project form
│   │   │   │   ├── ProjectManager.css# Project management styling
│   │   │   │   └── index.js          # Export barrel for project manager components
│   │   │   │
│   │   │   ├── OrderManagement/
│   │   │   │   ├── OrderList.js      # Designer's incoming orders list
│   │   │   │   ├── OrderDetail.js    # Detailed order view and status management
│   │   │   │   ├── OrderResponse.js  # Accept/decline order interface
│   │   │   │   ├── OrderManagement.css# Order management styling
│   │   │   │   └── index.js          # Export barrel for order management components
│   │   │   │
│   │   │   ├── Analytics/
│   │   │   │   ├── EarningsChart.js  # Designer earnings visualization
│   │   │   │   ├── ProjectStats.js   # Project completion statistics
│   │   │   │   ├── ClientFeedback.js # Client reviews and ratings display
│   │   │   │   ├── Analytics.css     # Analytics dashboard styling
│   │   │   │   └── index.js          # Export barrel for analytics components
│   │   │   │
│   │   │   └── Communication/
│   │   │       ├── MessageCenter.js  # Designer-client messaging interface
│   │   │       ├── NotificationList.js# Designer notifications and alerts
│   │   │       ├── Communication.css # Communication components styling
│   │   │       └── index.js          # Export barrel for communication components
│   │   │
│   │   └── customer/                 # Customer dashboard components
│   │       ├── CustomerProfile/
│   │       │   ├── CustomerProfile.js# Customer profile management
│   │       │   ├── PreferenceSettings.js# Customer preferences and settings
│   │       │   ├── AddressBook.js    # Manage shipping addresses
│   │       │   ├── CustomerProfile.css# Customer profile styling
│   │       │   └── index.js          # Export barrel for customer profile components
│   │       │
│   │       ├── OrderHistory/
│   │       │   ├── OrderHistory.js   # Customer's past orders display
│   │       │   ├── OrderTracking.js  # Track current order status
│   │       │   ├── OrderDetails.js   # Detailed view of individual orders
│   │       │   ├── OrderHistory.css  # Order history styling
│   │       │   └── index.js          # Export barrel for order history components
│   │       │
│   │       ├── Wishlist/
│   │       │   ├── Wishlist.js       # Customer wishlist management
│   │       │   ├── WishlistItem.js   # Individual wishlist item component
│   │       │   ├── Wishlist.css      # Wishlist styling
│   │       │   └── index.js          # Export barrel for wishlist components
│   │       │
│   │       ├── Reviews/
│   │       │   ├── ReviewForm.js     # Submit product/service reviews
│   │       │   ├── ReviewList.js     # Display customer's reviews
│   │       │   ├── ReviewItem.js     # Individual review display
│   │       │   ├── Reviews.css       # Review components styling
│   │       │   └── index.js          # Export barrel for review components
│   │       │
│   │       └── Support/
│   │           ├── SupportTickets.js # Customer support ticket management
│   │           ├── LiveChat.js       # Live chat support interface
│   │           ├── FAQ.js            # Frequently asked questions
│   │           ├── Support.css       # Support components styling
│   │           └── index.js          # Export barrel for support components
│   │
│   ├── pages/                        # Page-level components and views
│   │   ├── Home/
│   │   │   ├── Home.js               # Landing page with hero section and featured content
│   │   │   ├── Home.css              # Home page specific styling
│   │   │   └── index.js              # Export barrel for Home page
│   │   │
│   │   ├── Auth/
│   │   │   ├── Login.js              # Login page layout and logic
│   │   │   ├── Register.js           # Registration page layout
│   │   │   ├── ForgotPasswordPage.js # Forgot password page
│   │   │   ├── ResetPasswordPage.js  # Reset password page
│   │   │   ├── Auth.css              # Authentication pages styling
│   │   │   └── index.js              # Export barrel for auth pages
│   │   │
│   │   ├── Marketplace/
│   │   │   ├── MarketplacePage.js    # Main marketplace browsing page
│   │   │   ├── ProductPage.js        # Individual product detail page
│   │   │   ├── CategoryPage.js       # Category-specific product listings
│   │   │   ├── SearchResults.js      # Search results page
│   │   │   ├── CheckoutPage.js       # Checkout process page
│   │   │   ├── Marketplace.css       # Marketplace pages styling
│   │   │   └── index.js              # Export barrel for marketplace pages
│   │   │
│   │   ├── Designer/
│   │   │   ├── DesignerDashboard.js  # Main designer dashboard page
│   │   │   ├── DesignerProfilePage.js# Designer profile management page
│   │   │   ├── ProjectsPage.js       # Designer projects management page
│   │   │   ├── OrdersPage.js         # Designer orders page
│   │   │   ├── AnalyticsPage.js      # Designer analytics and reports page
│   │   │   ├── Designer.css          # Designer pages styling
│   │   │   └── index.js              # Export barrel for designer pages
│   │   │
│   │   ├── Customer/
│   │   │   ├── CustomerDashboard.js  # Main customer dashboard page
│   │   │   ├── CustomerProfilePage.js# Customer profile management page
│   │   │   ├── OrderHistoryPage.js   # Customer order history page
│   │   │   ├── WishlistPage.js       # Customer wishlist page
│   │   │   ├── SupportPage.js        # Customer support page
│   │   │   ├── Customer.css          # Customer pages styling
│   │   │   └── index.js              # Export barrel for customer pages
│   │   │
│   │   └── Error/
│   │       ├── NotFound.js           # 404 error page
│   │       ├── ServerError.js        # 500 server error page
│   │       ├── Unauthorized.js       # 401 unauthorized access page
│   │       ├── Error.css             # Error pages styling
│   │       └── index.js              # Export barrel for error pages
│   │
│   ├── store/                        # Redux store configuration and slices
│   │   ├── index.js                  # Main store configuration with middleware
│   │   ├── rootReducer.js            # Combines all slice reducers
│   │   │
│   │   ├── slices/
│   │   │   ├── authSlice.js          # Authentication state management (user, tokens, login status)
│   │   │   ├── userSlice.js          # User profile and preferences state
│   │   │   ├── marketplaceSlice.js   # Marketplace data (products, categories, filters)
│   │   │   ├── cartSlice.js          # Shopping cart state and operations
│   │   │   ├── orderSlice.js         # Order management and history state
│   │   │   ├── designerSlice.js      # Designer-specific state (projects, portfolio)
│   │   │   ├── customerSlice.js      # Customer-specific state (wishlist, reviews)
│   │   │   ├── uiSlice.js            # UI state (modals, loading, notifications)
│   │   │   └── searchSlice.js        # Search functionality and filters state
│   │   │
│   │   └── middleware/
│   │       ├── authMiddleware.js     # JWT token handling and auth state persistence
│   │       ├── apiMiddleware.js      # API call interceptors and error handling
│   │       └── loggingMiddleware.js  # Redux action logging for development
│   │
│   ├── services/                     # API service layer and external integrations
│   │   ├── api/
│   │   │   ├── client.js             # Axios client configuration with interceptors
│   │   │   ├── authAPI.js            # Authentication API calls (login, register, refresh)
│   │   │   ├── userAPI.js            # User profile and settings API calls
│   │   │   ├── marketplaceAPI.js     # Product and marketplace API calls
│   │   │   ├── orderAPI.js           # Order management API calls
│   │   │   ├── designerAPI.js        # Designer-specific API calls
│   │   │   ├── customerAPI.js        # Customer-specific API calls
│   │   │   ├── uploadAPI.js          # File upload and media management
│   │   │   └── searchAPI.js          # Search and filtering API calls
│   │   │
│   │   ├── websocket/
│   │   │   ├── socketClient.js       # WebSocket connection management
│   │   │   ├── messageHandlers.js    # WebSocket message processing
│   │   │   └── notifications.js      # Real-time notification handling
│   │   │
│   │   └── external/
│   │       ├── paymentService.js     # Payment processor integration (Stripe, PayPal)
│   │       ├── analyticsService.js   # Analytics tracking service integration
│   │       └── emailService.js       # Email service integration for notifications
│   │
│   ├── utils/                        # Utility functions and helpers
│   │   ├── auth/
│   │   │   ├── tokenManager.js       # JWT token storage and validation utilities
│   │   │   ├── authGuards.js         # Route protection and permission checking
│   │   │   └── roleUtils.js          # User role and permission utilities
│   │   │
│   │   ├── formatting/
│   │   │   ├── dateFormatter.js      # Date and time formatting utilities
│   │   │   ├── currencyFormatter.js  # Currency and price formatting
│   │   │   ├── textFormatter.js      # Text truncation and formatting
│   │   │   └── numberFormatter.js    # Number formatting and calculations
│   │   │
│   │   ├── validation/
│   │   │   ├── formValidators.js     # Form input validation functions
│   │   │   ├── emailValidator.js     # Email format validation
│   │   │   ├── passwordValidator.js  # Password strength validation
│   │   │   └── fileValidator.js      # File upload validation (size, type)
│   │   │
│   │   ├── helpers/
│   │   │   ├── arrayHelpers.js       # Array manipulation and processing utilities
│   │   │   ├── objectHelpers.js      # Object manipulation utilities
│   │   │   ├── urlHelpers.js         # URL generation and parsing utilities
│   │   │   └── storageHelpers.js     # LocalStorage and SessionStorage utilities
│   │   │
│   │   └── constants/
│   │       ├── apiEndpoints.js       # API endpoint constants
│   │       ├── routePaths.js         # Application route path constants
│   │       ├── userRoles.js          # User role and permission constants
│   │       └── appConfig.js          # Application configuration constants
│   │
│   ├── hooks/                        # Custom React hooks
│   │   ├── useAuth.js                # Authentication state and actions hook
│   │   ├── useLocalStorage.js        # LocalStorage management hook
│   │   ├── useDebounce.js            # Input debouncing hook
│   │   ├── useInfiniteScroll.js      # Infinite scrolling implementation hook
│   │   ├── useWebSocket.js           # WebSocket connection management hook
│   │   ├── useCart.js                # Shopping cart operations hook
│   │   └── useApi.js                 # API call management and caching hook
│   │
│   ├── context/                      # React context providers
│   │   ├── AuthContext.js            # Authentication context provider
│   │   ├── ThemeContext.js           # Theme and styling context provider
│   │   ├── NotificationContext.js    # Global notification system context
│   │   └── CartContext.js            # Shopping cart context provider
│   │
│   ├── styles/                       # Global styles and theme configuration
│   │   ├── globals.css               # Global CSS reset, base styles, and utilities
│   │   ├── variables.css             # CSS custom properties for colors, spacing, fonts
│   │   ├── themes/
│   │   │   ├── light.css             # Light theme color scheme
│   │   │   ├── dark.css              # Dark theme color scheme
│   │   │   └── index.js              # Theme switching utilities
│   │   │
│   │   ├── components/
│   │   │   ├── buttons.css           # Button component styling variations
│   │   │   ├── forms.css             # Form component styling
│   │   │   ├── cards.css             # Card component styling
│   │   │   └── navigation.css        # Navigation component styling
│   │   │
│   │   └── utilities/
│   │       ├── spacing.css           # Margin and padding utility classes
│   │       ├── typography.css        # Text styling utility classes
│   │       ├── layout.css            # Layout utility classes (flexbox, grid)
│   │       └── responsive.css        # Responsive design utility classes
│   │
│   └── assets/                       # Static assets and media files
│       ├── images/
│       │   ├── logo/
│       │   │   ├── logo.svg          # Main application logo (scalable)
│       │   │   ├── logo-dark.svg     # Dark theme logo variant
│       │   │   └── favicon.ico       # Website favicon
│       │   │
│       │   ├── placeholders/
│       │   │   ├── user-avatar.png   # Default user avatar placeholder
│       │   │   ├── product-placeholder.jpg# Default product image placeholder
│       │   │   └── banner-placeholder.jpg# Default banner image placeholder
│       │   │
│       │   ├── icons/
│       │   │   ├── social/           # Social media platform icons
│       │   │   ├── ui/               # User interface icons (arrows, buttons)
│       │   │   └── categories/       # Product category icons
│       │   │
│       │   └── backgrounds/
│       │       ├── hero-bg.jpg       # Homepage hero section background
│       │       ├── pattern-bg.svg    # Decorative background patterns
│       │       └── texture-bg.jpg    # Subtle texture backgrounds
│       │
│       ├── fonts/
│       │   ├── primary/              # Primary font family files
│       │   │   ├── font-regular.woff2# Regular weight font file
│       │   │   ├── font-bold.woff2   # Bold weight font file
│       │   │   └── font-light.woff2  # Light weight font file
│       │   │
│       │   └── secondary/            # Secondary font family files
│       │       ├── font-regular.woff2# Regular weight secondary font
│       │       └── font-bold.woff2   # Bold weight secondary font
│       │
│       └── data/
│           ├── mockData.js           # Mock data for development and testing
│           ├── sampleProducts.json   # Sample product data
│           └── categories.json       # Product category data
│
├── package.json                      # NPM package configuration with dependencies and scripts
├── package-lock.json                 # Locked dependency versions for consistent installs
│
├── .gitignore                        # Git ignore file for excluding build files, node_modules
├── .env                              # Environment variables (API URLs, keys)
├── .env.local                        # Local environment overrides (not committed)
├── .env.production                   # Production environment variables
│
├── README.md                         # Project documentation and setup instructions
├── .eslintrc.js                      # ESLint configuration for code quality
├── .prettierrc                       # Prettier configuration for code formatting
├── jsconfig.json                     # JavaScript project configuration for IDE support
│
└── build/                            # Production build output (generated)

DETAILED FILE DESCRIPTIONS:
===========================

ROOT CONFIGURATION FILES:
--------------------------

package.json:
- Project metadata and npm configuration
- Dependencies: React 18+, Redux Toolkit, React Router, Axios, Material-UI/Styled Components
- DevDependencies: ESLint, Prettier, Jest, React Testing Library
- Scripts: start, build, test, eject, lint, format
- Browserslist configuration for target browser support

.gitignore:
- Excludes node_modules, build directory, environment files
- IDE-specific files and OS-generated files
- Log files and temporary files

public/index.html:
- Single-page application HTML template
- Meta tags for SEO and responsive design
- Root div element where React app mounts
- External script references (fonts, analytics)

MAIN APPLICATION ENTRY POINTS:
------------------------------

src/index.js:
- Application bootstrap and DOM rendering
- React.StrictMode wrapper for development checks
- Service worker registration for PWA functionality
- Global error boundary setup

src/App.js:
- Main application component with routing logic
- Provider wrappers (Redux, Theme, Auth contexts)
- Global layout structure (Header, main content, Footer)
- Route definitions and protected route handling
- Global error boundary and loading states

COMPONENT ORGANIZATION:
-----------------------

Common Components (src/components/common/):
- Highly reusable UI components used throughout the application
- Consistent styling and behavior patterns
- Accessibility-focused implementation
- Responsive design considerations

Feature-Specific Components:
- Auth: Complete authentication flow components
- Marketplace: E-commerce functionality components
- Designer: Designer-specific dashboard and management tools
- Customer: Customer-focused interface components

REDUX STORE ARCHITECTURE:
-------------------------

Store Configuration (src/store/):
- Redux Toolkit for simplified state management
- Configured with Redux DevTools and middleware
- Persistence middleware for auth and cart state
- Immutable state updates with Immer

State Slices:
- Modular state management with separate slices
- Actions and reducers co-located
- Async thunks for API operations
- Optimistic updates for better UX

SERVICES AND API LAYER:
-----------------------

API Services (src/services/api/):
- Centralized API communication layer
- Axios client with request/response interceptors
- Error handling and retry logic
- Request/response transformation

External Services:
- Payment processing integration
- Real-time communication via WebSocket
- Third-party service integrations

UTILITIES AND HELPERS:
----------------------

Authentication Utilities:
- JWT token management and validation
- Route protection and role-based access
- Secure token storage practices

Validation and Formatting:
- Client-side form validation
- Data formatting for display
- Input sanitization and security

STYLING ARCHITECTURE:
--------------------

Global Styles:
- CSS custom properties for consistent theming
- Responsive design system with breakpoints
- Utility classes for common styling patterns

Component Styles:
- Co-located CSS files with components
- CSS modules or styled-components approach
- Theme-aware styling system

ASSETS ORGANIZATION:
-------------------

Images:
- Optimized images in multiple formats (WebP, JPEG, PNG)
- Responsive image sets for different screen densities
- SVG icons for scalability and performance

Fonts:
- Web-optimized font formats (WOFF2, WOFF)
- Font display optimization for performance
- Fallback font stacks for reliability

This structure provides a scalable, maintainable React.js application with clear separation of concerns, reusable components, and a robust state management system suitable for a comprehensive marketplace platform with designer and customer dashboards.
