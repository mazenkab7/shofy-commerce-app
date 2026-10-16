# 🛍️ Shofy - Modern eCommerce Platform

![Shofy eCommerce Platform](./public/thumbnail.png)

A modern, full-stack eCommerce application built with **Next.js 15**, **TypeScript**, **Firebase**, and **NextAuth.js**. Featuring a comprehensive admin dashboard, role-based authentication, and a responsive design.

![Next.js](https://img.shields.io/badge/Next.js-15.4.6-black?logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9.2-blue?logo=typescript)
![Firebase](https://img.shields.io/badge/Firebase-12.1.0-orange?logo=firebase)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-4.1.11-38B2AC?logo=tailwind-css)
![NextAuth](https://img.shields.io/badge/NextAuth.js-5.0.0-green?logo=auth0)

## 🚀 Quick Start

Get your eCommerce store running in minutes:

```bash
# 1. Clone the repository
git clone https://github.com/noorjsdivs/shofy-commerce-app-yt.git
cd shofy-commerce-app-yt

# 2. Install dependencies
npm install

# 3. Set up environment variables (see setup guide below)
cp .env.example .env.local
# Fill in your credentials

# 4. Start development server
npm run dev

# 5. Open your browser
# Visit: http://localhost:3000
```

## ✨ Features

### � **eCommerce Core**

- **Product Catalog**: Browse products with categories, search, and filtering
- **Shopping Cart**: Add/remove items, quantity management, persistent cart
- **Checkout Process**: Secure payment integration with Stripe
- **Order Management**: Track orders, order history, and status updates
- **Wishlist/Favorites**: Save products for later purchase
- **User Profiles**: Manage personal information, addresses, and preferences

### 🔐 **Authentication & Authorization**

- **Multi-Provider Auth**: Google, GitHub, and Email/Password via NextAuth.js
- **Role-Based Access Control (RBAC)**:
  - **User**: Standard shopping experience
  - **Admin**: Full system access and management
  - **Accountant**: Financial data access
  - **Delivery**: Order fulfillment management
  - **Packer**: Warehouse and packing operations
- **Session Management**: Secure session handling with automatic sync
- **Profile Management**: Edit profiles, upload avatars, change passwords

### � **Admin Dashboard**

- **Analytics & Insights**: Revenue tracking, user analytics, sales charts
- **User Management**: View, edit, delete users with bulk operations
- **Order Management**: Process orders, update status, bulk operations
- **Product Management**: Add, edit, delete products and categories
- **Role Assignment**: Assign and manage user roles
- **System Statistics**: Real-time dashboard with key metrics

### 🎨 **Design & UX**

- **Responsive Design**: Mobile-first approach, works on all devices
- **Modern UI**: Clean, professional design with smooth animations
- **Dark/Light Mode**: Theme switching capabilities
- **Multi-Currency**: Support for different currencies with conversion
- **Multi-Language**: Internationalization ready
- **Loading States**: Skeleton loaders and smooth transitions
- **Toast Notifications**: Real-time feedback for user actions

### 🛠️ **Technical Features**

- **Server-Side Rendering (SSR)**: Fast initial page loads
- **Static Site Generation (SSG)**: Optimized performance for static content
- **API Routes**: RESTful API endpoints for all operations
- **Database**: Firebase Firestore for real-time data
- **File Storage**: Firebase Storage for images and files
- **State Management**: Redux Toolkit with persistence
- **Form Handling**: Advanced form validation and error handling
- **SEO Optimized**: Meta tags, sitemap generation, and structured data
- **Performance**: Code splitting, lazy loading, and optimization

### 📱 **Pages & Routes**

#### **Public Pages**

- **Home**: Featured products, categories, and promotional banners
- **Products**: Product listing with search, filters, and pagination
- **Product Details**: Detailed product view with images and specifications
- **Categories**: Browse products by category
- **About**: Company information and mission
- **Contact**: Contact form and company details
- **FAQs**: Frequently asked questions with search
- **Inquiry**: Customer inquiry form

#### **User Pages**

- **Account Dashboard**: Personal overview and quick actions
- **Profile**: Edit personal information and upload avatar
- **Orders**: Order history and tracking
- **Order Details**: Detailed order information
- **Addresses**: Manage shipping and billing addresses
- **Settings**: Account preferences and notifications
- **Cart**: Shopping cart management
- **Checkout**: Secure payment process
- **Favorites**: Saved products and wishlist

#### **Admin Pages**

- **Admin Dashboard**: System overview and analytics
- **User Management**: Comprehensive user administration
- **Order Management**: Order processing and fulfillment
- **Analytics**: Detailed business insights and reports

#### **Role-Specific Dashboards**

- **Accountant Dashboard**: Financial reports and revenue tracking
- **Delivery Dashboard**: Order delivery and logistics
- **Packer Dashboard**: Warehouse and packing operations
- **User Dashboard**: Standard user experience

## 🏗️ **Tech Stack**

### **Frontend**

- **Next.js 15.4.6** - React framework with App Router
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Smooth animations and transitions
- **React Icons** - Comprehensive icon library
- **React Hot Toast** - Beautiful notifications

### **Backend & Authentication**

- **NextAuth.js 5.0** - Complete authentication solution
- **Firebase Firestore** - NoSQL real-time database
- **Firebase Storage** - File and image storage
- **Firebase Admin** - Server-side operations
- **bcryptjs** - Password hashing

### **State Management**

- **Redux Toolkit** - Predictable state management
- **Redux Persist** - State persistence across sessions
- **React Redux** - React bindings for Redux

### **Development & Build Tools**

- **ESLint** - Code linting and quality
- **TypeScript** - Static type checking
- **PostCSS** - CSS processing
- **Next Sitemap** - Automatic sitemap generation
- **Wrangler** - Cloudflare deployment (optional)

## 📁 **Project Structure**

```
shofy-commerce-app-yt/
├── src/
│   ├── app/                           # Next.js 15 App Router
│   │   ├── (public)/                 # Public routes (no authentication required)
│   │   │   ├── about/                # About page
│   │   │   ├── contact/              # Contact page
│   │   │   ├── faqs/                 # FAQ page
│   │   │   └── inquiry/              # Customer inquiry
│   │   ├── (user)/                   # Protected user routes
│   │   │   ├── account/              # User account management
│   │   │   │   ├── admin/            # Admin dashboard (Premium)
│   │   │   │   ├── addresses/        # Address management
│   │   │   │   ├── notifications/    # User notifications
│   │   │   │   ├── orders/           # Order history
│   │   │   │   ├── payment/          # Payment methods
│   │   │   │   ├── profile/          # User profile
│   │   │   │   └── settings/         # Account settings
│   │   │   ├── cart/                 # Shopping cart
│   │   │   ├── categories/           # Product categories
│   │   │   ├── checkout/             # Checkout process
│   │   │   ├── favorite/             # Wishlist/Favorites
│   │   │   ├── offers/               # Special offers
│   │   │   └── products/             # Product pages
│   │   ├── api/                      # API routes
│   │   │   ├── admin/                # Admin API endpoints
│   │   │   └── auth/                 # Authentication API
│   │   ├── auth/                     # Authentication pages
│   │   ├── dashboard/                # Role-based dashboards
│   │   ├── delivery/                 # Public delivery info
│   │   ├── delivery-dashboard/       # Delivery staff dashboard
│   │   ├── packer-dashboard/         # Packer staff dashboard
│   │   ├── unauthorized/             # Unauthorized access page
│   │   ├── user-dashboard/           # User dashboard
│   │   ├── globals.css               # Global styles
│   │   └── layout.tsx                # Root layout
│   ├── components/                   # Reusable React components
│   │   ├── account/                  # Account-related components
│   │   ├── admin/                    # Admin dashboard components
│   │   ├── auth/                     # Authentication components
│   │   ├── cart/                     # Shopping cart components
│   │   ├── dashboard/                # Dashboard components
│   │   ├── header/                   # Header and navigation
│   │   ├── layout/                   # Layout components
│   │   ├── notifications/            # Notification components
│   │   ├── pages/                    # Page-specific components
│   │   ├── products/                 # Product-related components
│   │   ├── ui/                       # UI components (buttons, cards, etc.)
│   │   └── [Various Components]      # Core app components
│   ├── assets/                       # Static assets (images, fonts)
│   ├── contexts/                     # React Context providers
│   ├── hooks/                        # Custom React hooks
│   ├── lib/                          # Utility libraries
│   │   ├── auth/                     # Authentication utilities
│   │   ├── firebase/                 # Firebase configuration
│   │   └── rbac/                     # Role-based access control
│   ├── redux/                        # Redux state management
│   ├── types/                        # TypeScript type definitions
│   └── constants/                    # Application constants
├── public/                           # Static public assets
│   ├── thumbnail.png                 # Project preview image
│   ├── logo.png                      # App logo
│   ├── robots.txt                    # SEO robots file
│   └── [Other Assets]                # Images, icons, etc.
├── middleware.ts                     # Route protection middleware
├── auth.ts                          # NextAuth configuration
├── config.ts                        # App configuration
├── firebase.ts                      # Firebase client config
├── type.ts                          # Global type definitions
├── next.config.mjs                  # Next.js configuration
├── tailwind.config.ts               # Tailwind CSS config
├── tsconfig.json                    # TypeScript configuration
└── package.json                     # Dependencies and scripts
```

## 🚀 **Complete Setup Guide**

### **Prerequisites**

Before you begin, make sure you have:

- **Node.js 18+** and **npm** installed
- **Git** for cloning the repository
- A **Firebase account** (free tier available)
- A **Google Cloud Console** account (for OAuth)
- A **GitHub account** (for OAuth - optional)

### **Step-by-Step Installation**

#### 1. **Clone the Repository**

```bash
git clone https://github.com/noorjsdivs/shofy-commerce-app-yt.git
cd shofy-commerce-app-yt
```

#### 2. **Install Dependencies**

```bash
npm install
```

#### 3. **Environment Setup**

Create a `.env.local` file in the root directory:

```bash
touch .env.local
```

Add the following environment variables (see detailed setup below):

```env
# NextAuth Configuration
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your-secret-key-here

# Google OAuth (Required)
AUTH_GOOGLE_ID=your-google-client-id
AUTH_GOOGLE_SECRET=your-google-client-secret

# GitHub OAuth (Optional)
AUTH_GITHUB_ID=your-github-client-id
AUTH_GITHUB_SECRET=your-github-client-secret

# Firebase Configuration
NEXT_PUBLIC_FIREBASE_API_KEY=your-api-key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your-project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your-project-id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your-project.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your-sender-id
NEXT_PUBLIC_FIREBASE_APP_ID=your-app-id

# Firebase Admin SDK
FIREBASE_PROJECT_ID=your-project-id
FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\nYour-Private-Key-Here\n-----END PRIVATE KEY-----\n"
FIREBASE_CLIENT_EMAIL=your-service-account@your-project.iam.gserviceaccount.com
```

#### 4. **Start Development Server**

```bash
npm run dev
```

#### 5. **Open Your Browser**

Navigate to [http://localhost:3000](http://localhost:3000)

---

## 🔑 **Environment Credentials Setup**

### **🔥 Firebase Setup (Required)**

#### **Step 1: Create Firebase Project**

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Click **"Create a project"**
3. Enter project name (e.g., `shofy-ecommerce`)
4. Enable Google Analytics (optional)
5. Click **"Create project"**

#### **Step 2: Get Client Configuration**

1. In Firebase Console, click **⚙️ Project Settings**
2. Scroll to **"Your apps"** section
3. Click **"Add app"** → **"Web"** (</> icon)
4. Register app with nickname (e.g., `Shofy Web`)
5. Copy the config values:

```javascript
// Firebase Config Object
const firebaseConfig = {
  apiKey: "AIzaSyC...", // → NEXT_PUBLIC_FIREBASE_API_KEY
  authDomain: "project.firebaseapp.com", // → NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN
  projectId: "your-project-id", // → NEXT_PUBLIC_FIREBASE_PROJECT_ID
  storageBucket: "project.appspot.com", // → NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET
  messagingSenderId: "123456789", // → NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID
  appId: "1:123:web:abc123", // → NEXT_PUBLIC_FIREBASE_APP_ID
};
```

#### **Step 3: Setup Firestore Database**

1. In Firebase Console, go to **"Firestore Database"**
2. Click **"Create database"**
3. Choose **"Start in test mode"** (for development)
4. Select your preferred location
5. Click **"Enable"**

#### **Step 4: Setup Firebase Storage**

1. Go to **"Storage"** in Firebase Console
2. Click **"Get started"**
3. Choose **"Start in test mode"**
4. Select the same location as Firestore
5. Click **"Done"**

#### **Step 5: Get Admin SDK Credentials**

1. Go to **Project Settings** → **"Service accounts"** tab
2. Click **"Generate new private key"**
3. Download the JSON file
4. Extract these values for your `.env.local`:
   - `project_id` → `FIREBASE_PROJECT_ID`
   - `private_key` → `FIREBASE_PRIVATE_KEY` (keep \n characters)
   - `client_email` → `FIREBASE_CLIENT_EMAIL`

### **🔐 Google OAuth Setup (Required)**

#### **Step 1: Google Cloud Console**

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create new project or select existing Firebase project
3. Enable the project if prompted

#### **Step 2: Configure OAuth Consent Screen**

1. Go to **"APIs & Services"** → **"OAuth consent screen"**
2. Choose **"External"** → Click **"Create"**
3. Fill in required fields:
   - App name: `Shofy eCommerce`
   - User support email: your email
   - Developer contact: your email
4. Click **"Save and Continue"** through all steps

#### **Step 3: Create OAuth Credentials**

1. Go to **"APIs & Services"** → **"Credentials"**
2. Click **"+ CREATE CREDENTIALS"** → **"OAuth 2.0 Client IDs"**
3. Application type: **"Web application"**
4. Name: `Shofy Web Client`
5. Add **Authorized redirect URIs**:
   ```
   http://localhost:3000/api/auth/callback/google
   https://yourdomain.com/api/auth/callback/google
   ```
6. Click **"Create"**
7. Copy the **Client ID** and **Client Secret**:
   - Client ID → `AUTH_GOOGLE_ID`
   - Client Secret → `AUTH_GOOGLE_SECRET`

### **🐙 GitHub OAuth Setup (Optional)**

#### **Step 1: Create GitHub OAuth App**

1. Go to [GitHub Developer Settings](https://github.com/settings/developers)
2. Click **"New OAuth App"**
3. Fill in the form:
   - **Application name**: `Shofy eCommerce`
   - **Homepage URL**: `http://localhost:3000`
   - **Authorization callback URL**: `http://localhost:3000/api/auth/callback/github`
4. Click **"Register application"**

#### **Step 2: Get Credentials**

1. Copy **Client ID** → `AUTH_GITHUB_ID`
2. Click **"Generate a new client secret"**
3. Copy **Client Secret** → `AUTH_GITHUB_SECRET`

### **🔒 NextAuth Secret Generation**

Generate a secure secret for session encryption:

```bash
# Using Node.js
node -e "console.log(require('crypto').randomBytes(32).toString('base64'))"

# Or using OpenSSL
openssl rand -base64 32
```

Copy the generated string to `NEXTAUTH_SECRET`

### **✅ Verify Setup**

After adding all environment variables:

1. Restart your development server:

   ```bash
   npm run dev
   ```

2. Test authentication:
   - Visit `http://localhost:3000`
   - Click "Sign In"
   - Try Google OAuth login
   - Check if user data appears in Firebase Console

---

## 📋 **Available Scripts**

```bash
# Development
npm run dev          # Start development server on http://localhost:3000
npm run build        # Build optimized production bundle
npm run start        # Start production server (after build)
npm run lint         # Run ESLint for code quality
npm run type-check   # Run TypeScript type checking

# Utilities
npm run postbuild    # Generate sitemap after build
npm run deploy:check # Run deployment checks
npm run deploy:cf    # Deploy to Cloudflare Pages (if configured)
```

### **Development Workflow**

1. **Start Development**: `npm run dev`
2. **Check Code Quality**: `npm run lint`
3. **Type Safety**: `npm run type-check`
4. **Build for Production**: `npm run build`
5. **Test Production**: `npm run start`

## � **Admin Access Setup**

### **Method 1: Email-Based Admin (Recommended)**

Set admin email in your authentication logic:

1. **Register with your admin email**
2. **Check `AccountLayout.tsx`** - admin access is granted to:
   - `admin@shofy.com`
   - Users with `role: "admin"`

### **Method 2: Role-Based Admin**

1. **Register a new account**
2. **Go to Firebase Console** → Firestore Database
3. **Find your user document** in the `users` collection
4. **Add a field**: `role: "admin"`
5. **Save and refresh** your application

### **Admin Features**

- **🎯 Premium Feature**: Full admin dashboard is available in the premium version
- **📊 Dashboard**: Basic dashboard with upgrade prompt
- **🔗 Upgrade Link**: Direct link to purchase premium features
- **⚙️ Settings**: Standard account management

**Admin URL**: `http://localhost:3000/account/admin`

## 🌟 **Key Features Highlights**

### **Advanced Authentication**

- Multiple OAuth providers
- Role-based dashboard routing
- Session synchronization
- Secure middleware protection

### **Comprehensive Admin Panel**

- Real-time analytics
- Bulk operations for users and orders
- Advanced filtering and search
- Export capabilities

### **Enhanced UX**

- Skeleton loading states
- Optimistic UI updates
- Real-time notifications
- Responsive design patterns

### **Performance Optimizations**

- Image optimization with Next.js
- Code splitting and lazy loading
- Static generation where possible
- Efficient state management

## 🎨 **Customization Guide**

### **Branding & Styling**

1. **Colors**: Update `tailwind.config.ts` for brand colors
2. **Logo**: Replace files in `/public/` and `/src/assets/`
3. **Fonts**: Modify `/src/fonts/` directory
4. **Theme**: Customize CSS variables in `globals.css`

### **Content Customization**

1. **Homepage**: Edit components in `/src/components/pages/home/`
2. **Navigation**: Update `/src/components/header/`
3. **Footer**: Modify `/src/components/Footer.tsx`
4. **Static Pages**: Edit files in `/src/app/(public)/`

### **Feature Extensions**

1. **Payment Integration**: Add Stripe/PayPal in `/src/lib/`
2. **Email Service**: Integrate with SendGrid, Mailgun, etc.
3. **Analytics**: Add Google Analytics, Mixpanel, etc.
4. **Search**: Implement Algolia, Elasticsearch, etc.

### **API Customization**

1. **Endpoints**: Modify `/src/app/api/` routes
2. **Database**: Extend Firestore collections
3. **Authentication**: Add custom providers in `auth.ts`
4. **Middleware**: Update `/middleware.ts` for custom logic

## � **Deployment**

### **Vercel (Recommended)**

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/noorjsdivs/shofy-commerce-app-yt)

1. **Push to GitHub**:

   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Deploy to Vercel**:

   - Go to [Vercel Dashboard](https://vercel.com/dashboard)
   - Click "New Project"
   - Import your GitHub repository
   - Add environment variables
   - Deploy

3. **Update Environment**:
   - Set `NEXTAUTH_URL` to your Vercel domain
   - Update OAuth redirect URIs

### **Other Platforms**

- **Netlify**: Connect GitHub and deploy
- **Railway**: One-click deployment
- **Digital Ocean**: App Platform
- **AWS**: Amplify Hosting

### **Environment Variables for Production**

Remember to update these in production:

```env
NEXTAUTH_URL=https://your-domain.com
# Update OAuth redirect URIs in Google/GitHub console
# Use production Firebase project
```

## �📄 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 **Support & Help**

### **Getting Help**

1. **📖 Documentation**: This README covers everything you need
2. **🐛 Issues**: [Open a GitHub Issue](https://github.com/noorjsdivs/shofy-commerce-app-yt/issues)
3. **💬 Discussions**: [GitHub Discussions](https://github.com/noorjsdivs/shofy-commerce-app-yt/discussions)
4. **📧 Email**: [noorjsdivs@gmail.com](mailto:noorjsdivs@gmail.com)

### **Premium Support**

- **🎯 Admin Dashboard**: [Buy Premium Version](https://buymeacoffee.com/reactbd/e/448682)
- **🛠️ Custom Development**: Available for hire
- **📚 Training**: One-on-one setup assistance
- **🔧 Maintenance**: Ongoing support packages

### **Community**

- **⭐ Star this repo** if you find it helpful
- **🍴 Fork & contribute** improvements
- **📢 Share** with other developers

## 🙏 **Acknowledgments**

- **Next.js Team** - Amazing React framework
- **Firebase Team** - Reliable backend services
- **Tailwind CSS** - Beautiful utility-first CSS
- **NextAuth.js** - Secure authentication
- **Vercel** - Seamless deployment platform
- **Open Source Community** - Inspiration and tools

## 🤝 **Contributing**

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

**⭐ Star this repository if it helped you!**

**Built by Mazen Kabboul**

### 🎨 **Modern UI/UX**

- **Responsive Design** (Mobile-first approach)
- **Professional Animations** with Framer Motion
- **Loading Skeletons** for better UX
- **Toast Notifications** for user feedback
- **Dynamic Navigation** with mobile optimization
- **Professional Color Scheme** with consistent branding

### 📱 **Mobile Experience**

- **Mobile Navigation** with hamburger menu
- **Touch-Friendly** interface
- **Optimized Performance** for mobile devices
- **Progressive Web App** ready

## 🚀 Getting Started

### Prerequisites

- **Node.js** 18.0 or later
- **npm** or **pnpm** package manager
- **Firebase Account** (for database and authentication)
- **Google Cloud Console** account (for Google OAuth)
- **GitHub** account (for GitHub OAuth)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/noorjsdivs/shofy-commerce-app.git
   cd shofy-commerce-app
   ```

2. **Install dependencies**

   ```bash
   npm install
   # or
   pnpm install
   ```

3. **Set up environment variables** (see [Environment Setup](#-environment-setup) below)

4. **Run the development server**

   ```bash
   npm run dev
   # or
   pnpm dev
   ```

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🔧 Environment Setup

Create a `.env` file in the root directory and add the following variables:

```env
# NextAuth Configuration
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your-secret-key-here

# Google OAuth Configuration
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret

# GitHub OAuth Configuration
GITHUB_ID=your-github-client-id
GITHUB_SECRET=your-github-client-secret

# Firebase Client Configuration
NEXT_PUBLIC_FIREBASE_API_KEY=your-firebase-api-key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your-project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your-firebase-project-id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your-project.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your-sender-id
NEXT_PUBLIC_FIREBASE_APP_ID=your-app-id

# Firebase Admin SDK (for server-side operations)
FIREBASE_PROJECT_ID=your-firebase-project-id
FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\nYOUR_PRIVATE_KEY_HERE\n-----END PRIVATE KEY-----\n"
FIREBASE_CLIENT_EMAIL=your-service-account@your-project.iam.gserviceaccount.com

# Stripe Configuration (Optional)
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your-stripe-publishable-key
STRIPE_SECRET_KEY=your-stripe-secret-key
```

## 🔑 How to Obtain Environment Credentials

### 🔥 Firebase Setup

1. **Create a Firebase Project**

   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Click "Create a project"
   - Enter project name (e.g., "shofy-ecommerce")
   - Enable Google Analytics (optional)

2. **Get Firebase Client Configuration**

   - In Firebase Console, click "Add app" → "Web"
   - Register your app with a nickname
   - Copy the configuration object values:
     ```javascript
     const firebaseConfig = {
       apiKey: "your-api-key", // → NEXT_PUBLIC_FIREBASE_API_KEY
       authDomain: "your-project.firebaseapp.com", // → NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN
       projectId: "your-project-id", // → NEXT_PUBLIC_FIREBASE_PROJECT_ID
       storageBucket: "your-project.appspot.com", // → NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET
       messagingSenderId: "123456789", // → NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID
       appId: "your-app-id", // → NEXT_PUBLIC_FIREBASE_APP_ID
     };
     ```

3. **Set up Firestore Database**

   - Go to "Firestore Database" in Firebase Console
   - Click "Create database"
   - Choose "Start in test mode" (for development)
   - Select a location

4. **Get Firebase Admin SDK**
   - Go to Project Settings → Service Accounts
   - Click "Generate new private key"
   - Download the JSON file
   - Extract values:
     - `project_id` → `FIREBASE_PROJECT_ID`
     - `private_key` → `FIREBASE_PRIVATE_KEY` (keep the newlines as \n)
     - `client_email` → `FIREBASE_CLIENT_EMAIL`

### 🔐 Google OAuth Setup

1. **Go to Google Cloud Console**

   - Visit [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project or select existing one

2. **Enable Google+ API**

   - Go to "APIs & Services" → "Library"
   - Search for "Google+ API" and enable it

3. **Create OAuth 2.0 Credentials**
   - Go to "APIs & Services" → "Credentials"
   - Click "Create Credentials" → "OAuth 2.0 Client IDs"
   - Choose "Web application"
   - Add authorized redirect URIs:
     - `http://localhost:3000/api/auth/callback/google` (development)
     - `https://yourdomain.com/api/auth/callback/google` (production)
   - Copy the Client ID and Client Secret

### 🐙 GitHub OAuth Setup

1. **Go to GitHub Developer Settings**

   - Visit [GitHub Developer Settings](https://github.com/settings/developers)
   - Click "New OAuth App"

2. **Configure OAuth App**

   - **Application name**: Shofy E-Commerce
   - **Homepage URL**: `http://localhost:3000` (development)
   - **Authorization callback URL**: `http://localhost:3000/api/auth/callback/github`
   - Click "Register application"

3. **Get Credentials**
   - Copy the Client ID → `GITHUB_ID`
   - Generate a new client secret → `GITHUB_SECRET`

### 🔒 NextAuth Secret

Generate a secure secret for NextAuth:

```bash
# Using openssl
openssl rand -base64 32

# Using Node.js
node -e "console.log(require('crypto').randomBytes(32).toString('base64'))"
```

Copy the generated string to `NEXTAUTH_SECRET`

### 💳 Stripe Setup (Optional)

1. **Create Stripe Account**

   - Go to [Stripe Dashboard](https://dashboard.stripe.com/)
   - Create an account or log in

2. **Get API Keys**
   - Go to "Developers" → "API keys"
   - Copy "Publishable key" → `NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY`
   - Copy "Secret key" → `STRIPE_SECRET_KEY`

## 📁 Project Structure

```
shofy-commerce-app/
├── src/
│   ├── app/                    # Next.js 13+ App Router
│   │   ├── auth/              # Authentication pages
│   │   │   ├── signin/        # Sign in page
│   │   │   └── register/      # Registration page
│   │   ├── api/               # API routes
│   │   │   └── auth/          # Authentication API
│   │   ├── cart/              # Shopping cart page
│   │   ├── offers/            # Special offers page
│   │   ├── products/          # Product pages
│   │   └── profile/           # User profile page
│   ├── components/            # Reusable components
│   │   ├── auth/              # Authentication components
│   │   ├── cart/              # Cart components
│   │   ├── header/            # Header components
│   │   ├── pages/             # Page-specific components
│   │   └── ui/                # UI components
│   ├── lib/                   # Utility libraries
│   │   ├── auth/              # Authentication configuration
│   │   └── firebase/          # Firebase configuration
│   ├── redux/                 # State management
│   ├── constants/             # Application constants
│   └── assets/                # Static assets
├── public/                    # Public assets
├── .env                       # Environment variables
└── package.json               # Dependencies and scripts
```

## 🛠️ Technologies Used

### **Frontend**

- **Next.js 15.4.6** - React framework with App Router
- **TypeScript** - Type-safe JavaScript
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Animation library
- **React Icons** - Icon library
- **React Hot Toast** - Toast notifications

### **Authentication**

- **NextAuth.js** - Authentication framework
- **Firebase Auth** - Authentication provider
- **bcryptjs** - Password hashing

### **Database**

- **Firebase Firestore** - NoSQL document database
- **Firebase Storage** - File storage

### **State Management**

- **Redux Toolkit** - Predictable state container
- **React Redux** - React bindings for Redux

### **Development Tools**

- **ESLint** - Code linting
- **Prettier** - Code formatting
- **TypeScript** - Static type checking

## 🎯 Key Features Explained

### 🔐 Authentication Flow

1. **Registration**: Users create accounts with email/password or OAuth
2. **Verification**: Email verification (optional)
3. **Login**: Secure login with session management
4. **Protected Routes**: Middleware protects authenticated pages
5. **User Profile**: Complete profile management

### 🛒 Shopping Experience

1. **Product Browsing**: Advanced filtering and sorting
2. **Search**: Real-time product search
3. **Cart Management**: Add/remove items with quantity control
4. **Wishlist**: Save favorite products
5. **Checkout**: Secure payment processing (Stripe integration)

### 📱 Responsive Design

- **Mobile-First**: Optimized for mobile devices
- **Tablet Support**: Proper layout for tablets
- **Desktop**: Full-featured desktop experience
- **Cross-Browser**: Compatible with all modern browsers

## 🚀 Deployment

### Vercel Deployment (Recommended)

1. **Push to GitHub**

   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Deploy to Vercel**

   - Go to [Vercel Dashboard](https://vercel.com/dashboard)
   - Click "New Project"
   - Import your GitHub repository
   - Add environment variables
   - Deploy

3. **Update Environment Variables**
   - Update `NEXTAUTH_URL` to your Vercel domain
   - Update OAuth redirect URIs to match your domain

### Other Deployment Options

- **Netlify**
- **Railway**
- **Digital Ocean**
- **AWS**

## 🔧 Scripts

```bash
# Development
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run type-check   # Run TypeScript check
```

## 🤝 Contributing

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes**
   ```bash
   git commit -m "Add amazing feature"
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open a Pull Request**

## 📝 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Next.js Team** for the amazing framework
- **Firebase Team** for the backend services
- **Tailwind CSS** for the utility-first CSS framework
- **DummyJSON** for the product API
- **React Community** for the excellent ecosystem

## 🎉 Features Roadmap

- [ ] **Email Verification**
- [ ] **Password Reset**
- [ ] **Admin Dashboard**
- [ ] **Order Management**
- [ ] **Inventory Management**
- [ ] **Product Reviews**
- [ ] **Advanced Analytics**
- [ ] **Multi-language Support**
- [ ] **Dark Mode**
- [ ] **PWA Features**

---

**Built by Mazen Kabboul**

**⭐ Star this repository if you find it helpful!**
