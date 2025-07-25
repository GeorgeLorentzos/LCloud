# LCloud
- A secure and feature-rich Python Flask web application for cloud-based file storage and management, offering user authentication, file operations, subscription plans, and email verification.

## Key Features  
### Security & Authentication  
- Multi-layer user authentication with Flask-Login and bcrypt hashing  
- Complete email verification system for new account activation  
- Secure password recovery with time-limited tokens  
- CSRF protection on all forms

### Account Management
- User registration with email verification
- Profile editing (username, email, password)
- Account deletion with complete data purge
- Timezone settings per user account
- Email verification required for login
- Password complexity enforcement

### File Management  
- User-isolated storage with dedicated folders  
- Intelligent quota system (2GB free / 10GB premium)  
- Secure file handling with Werkzeug's secure_filename()  
- Timezone-aware timestamps (pytz integration)
- File renaming
- File deletion
- File size validation
- Duplicate file prevention

### Subscription & Payments  
- Stripe integration for premium subscriptions  
- Automated billing portal for customers  
- Webhook handling for payment events  
- Tiered storage plans with automatic upgrades/downgrades  

### Email System  
- SMTP integration with TLS encryption  
- Custom HTML templates for verification/reset emails  
- Async email delivery (using Flask-Mail)
- Token expiration system

## Usage
1. Clone this repository:
    ```bash
    https://github.com/GeorgeLorentzos/LCloud.git
    cd lcloud
    ```
2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Create a .env file and set up the environment variables with the following content:
    ```
    SECRET_KEY=your_secret_key
    MAIL_USERNAME=your_email@gmail.com
    MAIL_PASSWORD=your_app_password
    STRIPE_SECRET_KEY=your_stripe_secret_key
    STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key
    STRIPE_WEBHOOK_SECRET=your_webhook_secret
    ```
4. Run the application:
    ```bash
    python app.py
    ```

## Sneak Peek of the App — 3 Screenshots

<img src="static/lcloud_preview/dashboard.png" alt="Dashboard Preview" style="max-width: 100%; border-radius: 8px;" />
</br>
<img src="static/lcloud_preview/account_settings.png" alt="Dashboard Preview" style="max-width: 100%; border-radius: 8px;" />
</br>
<img src="static/lcloud_preview/account_verify.png" alt="Dashboard Preview" style="max-width: 100%; border-radius: 8px;" />
