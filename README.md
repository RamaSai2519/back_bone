# Sukoon Backend Platform

A comprehensive AWS Amplify-based backend platform built with Python Flask, providing a complete suite of APIs and automated jobs for a mental health and wellness application ecosystem.

## 🏗️ Architecture

The platform consists of two main AWS Lambda functions:

### 1. **gamesProcessor** - Main API Server
A Flask-based RESTful API server handling all business logic and user interactions.

### 2. **scheduler** - Automated Job Scheduler
Event-driven Lambda function for executing scheduled tasks and background jobs.

## 🚀 Core Features & Capabilities

### 👥 User Management
- **User CRUD Operations**: Create, read, update user profiles with detailed demographics and psychographics
- **User Engagement Tracking**: Monitor and update user engagement data
- **User Referral System**: Track referrals and user acquisition channels
- **User Vacation Management**: Handle expert/therapist vacation schedules
- **Beta Tester Management**: Manage beta testing program participants
- **Phone Configuration**: User device and phone settings management
- **User Status Options**: Customizable user status and availability settings

### 🧠 Mental Health Expert System
- **Expert Profiles**: Comprehensive expert/therapist profile management
- **Applicant Management**: Handle expert applications and onboarding
- **Slot Management**: Dynamic scheduling and availability management
- **Timings Configuration**: Customizable working hours and schedules
- **Expert Scoring System**: Automated performance evaluation and scoring
- **Agent Metadata**: Track call metadata and expert performance metrics
- **Category Management**: Expertise categories and specializations

### 📞 Call & Communication System
- **Voice Call Management**: Initiate and manage voice calls
- **Call Webhooks**: Real-time call status updates and event handling
- **Escalation System**: Automated issue escalation workflows
- **SCall Integration**: Advanced call platform integration with multiple webhook endpoints
- **Slack Integration**: Real-time notifications and alerts to Slack channels
- **Call Recording & Analytics**: Track call metrics and performance

### 💬 WhatsApp Integration
- **Message Sending**: Send WhatsApp messages via API
- **Webhook Handlers**: Process incoming WhatsApp messages and events
- **Template Management**: Create and manage WhatsApp message templates
- **Message References**: Track WhatsApp message references and threads
- **WhatsApp Options**: Configure WhatsApp settings and options
- **Message History**: Complete WhatsApp conversation tracking and history

### 📅 Events Management
- **Event Configuration**: Create and manage mental health events and workshops
- **Event Users**: Participant registration and management
- **Event Webhooks**: Real-time event updates and notifications
- **Contribute Events**: Community contribution and volunteering events
- **Interest Management**: Track user interest in events and activities

### 💰 Payment & Subscriptions
- **Cashfree Integration**: Complete payment gateway integration
- **Payment Orders**: Create and manage payment orders
- **Payment Webhooks**: Handle payment status updates
- **Subscription Plans**: Flexible subscription plan management
- **User Balance Management**: Track and update user wallet/credits
- **Eligibility Checks**: Verify user eligibility for services
- **Offer Redemption**: Coupon and offer management system

### 🎮 Gamification & Engagement
- **Quiz Games**: Interactive quiz game system
- **Game Play Tracking**: Save and track game sessions
- **Leaderboards**: Competitive ranking and achievements
- **Quiz Questions Management**: Dynamic question bank management
- **Card Games**: Traditional card game implementations
- **Game History**: Complete game activity tracking
- **Score Updates**: Real-time score calculation and updates
- **Winner Calculation**: Automated winner determination
- **Coupon Rewards**: Reward system for game achievements

### 📝 Content Management System
- **Chat System**: AI-powered chat functionality
- **Photo Management**: Image upload, storage, and retrieval
- **Blog Posts**: Create and manage blog content
- **Songs/Audio**: Music and audio content management
- **Content Posts**: General content posting and management
- **DALL-E Integration**: AI-powered image generation
- **Shorts/Videos**: Short-form video content management

### 🔔 Push Notifications
- **FCM Integration**: Firebase Cloud Messaging integration
- **Push Notification Sending**: Targeted push notification delivery
- **FCM Token Management**: Device token registration and updates
- **Notification Templates**: Reusable notification templates
- **BytePlus Integration**: Alternative push notification provider

### 📊 Analytics & Reporting
- **Dashboard Statistics**: Comprehensive admin dashboard metrics
- **Engagement Analytics**: User engagement and activity reports
- **Lead Tracking**: Lead generation and conversion tracking
- **Lead Counts**: Aggregate lead statistics
- **Error Logs**: Centralized error logging and monitoring
- **Platform Categories**: Category-wise analytics

### 🔐 Authentication & Security
- **OTP System**: Send and validate one-time passwords
- **JWT Authentication**: Secure token-based authentication
- **Admin Authentication**: Separate admin access control
- **Phone Number Validation**: Verify user phone numbers

### 📋 Administrative Tools
- **File Upload (S3)**: Secure file storage and retrieval
- **Error Logging**: Comprehensive error tracking
- **Remarks System**: Add notes and remarks to records
- **WhatsApp Admin Panel**: Administrative WhatsApp management interface
- **FCM Admin Tools**: Manage admin push notification settings
- **System Prompts**: Configure AI system prompts and templates

### 🤖 Automated Scheduler Jobs

The scheduler function runs periodic background tasks:

1. **Recurring Schedules**: Process recurring appointments and schedules
2. **Schedule Management**: Handle one-time scheduled tasks
3. **Event Reminders**: Send automated event reminder notifications
4. **Events Reminders Lister**: Identify upcoming events requiring reminders
5. **Auto Online Status**: Automatically update expert online/offline status
6. **Expert Status Job**: Periodic expert availability checks
7. **Email Reader**: Process incoming emails for leads and inquiries
8. **Database Backup**: Automated database backup job
9. **WhatsApp Job Handler**: Process queued WhatsApp messages

### 🔧 Technical Capabilities

- **Parallel Job Execution**: ThreadPoolExecutor for concurrent task processing
- **GraphQL Support**: GraphQL integration for flexible queries
- **CORS Enabled**: Cross-origin resource sharing for web applications
- **JWT Token Management**: Secure authentication with refresh tokens
- **MongoDB Integration**: NoSQL database for flexible data storage
- **S3 Integration**: AWS S3 for file storage and media
- **Firebase Admin SDK**: Firebase authentication and services
- **OpenAI Integration**: AI-powered features and chat
- **Slack SDK**: Team collaboration and notifications
- **Google Auth**: OAuth integration for Google services

## 🛠️ Technology Stack

### Backend Framework
- **Flask** 3.0.2 - Web framework
- **Flask-RESTful** 0.3.10 - REST API framework
- **Flask-CORS** 4.0.0 - CORS handling
- **Flask-JWT-Extended** 4.6.0 - JWT authentication

### Database & Storage
- **PyMongo** 4.8.0 - MongoDB driver
- **AWS S3** - File storage via aws-wsgi

### External Integrations
- **OpenAI** 1.45.0 - AI capabilities
- **Firebase Admin** 6.5.0 - Firebase services
- **Slack SDK** 3.33.1 - Slack integration
- **GraphQL** (gql 3.5.0) - GraphQL client

### Infrastructure
- **AWS Lambda** - Serverless compute
- **AWS Amplify** - Backend management
- **AWS WSGI** 0.2.7 - Lambda-Flask adapter

### Security & Auth
- **Bcrypt** 3.2.2 - Password hashing
- **Cryptography** 3.4.8 - Encryption
- **Google Auth** 2.31.0 - OAuth

### Utilities
- **Requests** 2.32.3 - HTTP library
- **Requests-AWS4Auth** 1.2.3 - AWS request signing
- **PyTZ** 2024.1 - Timezone handling
- **urllib3** 1.26.6 - HTTP client

## 📁 Project Structure

```
backend_amp/
├── amplify/
│   └── backend/
│       └── function/
│           ├── gamesProcessor/          # Main API Lambda
│           │   └── src/
│           │       ├── index.py         # Flask app entry point
│           │       ├── models/          # 100+ API endpoint models
│           │       ├── services/        # Business logic services
│           │       └── shared/          # Common utilities
│           └── scheduler/               # Scheduler Lambda
│               └── src/
│                   ├── index.py         # Scheduler entry point
│                   ├── models/          # Job implementations
│                   └── shared/          # Common utilities
└── src/
    └── graphql/                         # GraphQL schemas
```

## 🔑 Key Modules

### Services (Business Logic)
- `user.py` - User management operations
- `expert.py` - Expert/therapist management
- `call.py` - Voice call handling
- `whatsapp.py` - WhatsApp messaging
- `events.py` - Event management
- `payment.py` - Payment processing
- `subscription.py` - Subscription management
- `games.py` - Quiz and game features
- `content.py` - Content management
- `push_notification.py` - Push notifications
- `authenticate.py` - Authentication services
- `admin.py` - Administrative functions
- `dashboard.py` - Analytics and reporting
- `leads.py` - Lead management

### Models (API Endpoints)
117 specialized API endpoint implementations including:
- User operations (get, upsert, delete history)
- Expert management (slots, timings, applicants, vacations)
- Call handling (make call, webhooks, escalation)
- WhatsApp (send, webhook, templates, refs)
- Events (list, upsert, users, contributions)
- Payments (create order, webhooks, Cashfree)
- Games (quiz, leaderboard, questions, save play)
- Content (chat, photos, blog, songs, DALL-E)
- And many more...

## 🎯 Use Cases

This backend supports a comprehensive mental health platform enabling:

1. **Therapy Sessions**: Connect users with mental health experts via voice calls
2. **Scheduled Appointments**: Book and manage therapy sessions
3. **Community Events**: Host and participate in wellness events
4. **Educational Content**: Access blog posts, videos, and educational materials
5. **Gamified Wellness**: Engage users through interactive quizzes and games
6. **Subscription Services**: Monetize through flexible subscription plans
7. **Lead Generation**: Capture and manage potential user inquiries
8. **Automated Reminders**: Keep users engaged with timely notifications
9. **Expert Marketplace**: Browse and connect with qualified therapists
10. **Community Support**: Foster peer support through events and contributions

## 🚦 Getting Started

### Prerequisites
- **Python 3.9 or higher** (minimum 3.8 supported, but 3.9+ recommended for best performance)
- **AWS Account** with Amplify CLI configured
- **MongoDB** instance (local or cloud-hosted like MongoDB Atlas)
- **API Keys** and credentials for:
  - OpenAI API (for AI chat features)
  - Firebase (for authentication and FCM)
  - Slack (for notifications)
  - Cashfree (for payment processing)
  - WhatsApp Business API (for messaging)
  - AWS credentials (for S3 and Lambda deployment)

### Installation
```bash
cd backend_amp/amplify/backend/function/gamesProcessor/src
pip install -r requirements.txt
```

### Local Development
```bash
# Run the main API server locally
python index.py
# Server will start on http://localhost:8080
```

### Testing Scheduler
```bash
cd backend_amp/amplify/backend/function/scheduler/src
python index.py
```

## 📝 API Documentation

The API follows RESTful conventions with endpoints structured as:
- `POST /actions/{resource}` - Create/Update operations
- `GET /actions/{resource}` - Read operations

All responses follow a standardized output format with:
- `output_status` - SUCCESS/FAILURE
- `output_message` - Descriptive message
- `output_details` - Response data

## 🔒 Security Features

- JWT-based authentication for user endpoints
- Admin-specific JWT authentication for admin endpoints
- OTP verification for phone number validation
- Bcrypt password hashing
- CORS configuration for web security
- AWS IAM roles for Lambda permissions
- Encrypted sensitive data handling

## 🌟 Highlights

- **Scalable Architecture**: AWS Lambda serverless design handles variable load automatically
- **Comprehensive API**: 140+ endpoints covering all platform needs
- **Real-time Processing**: Webhook integrations for instant updates
- **Automated Jobs**: Scheduled tasks run independently without manual intervention
- **Multi-channel Communication**: Voice, WhatsApp, Push, Email integration
- **Extensible Design**: Modular structure allows easy feature additions
- **Production Ready**: Error handling, logging, and monitoring built-in

## 📞 Support & Contact

For questions or issues related to this backend platform, please refer to the code documentation or contact the development team.

---

*Backend for Sukoon - Find peace in the code, deliver peace through technology.* 🧘‍♀️✨
