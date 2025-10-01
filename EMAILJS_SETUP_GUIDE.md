# EmailJS Setup Guide for Dukaan Setu

## Step 1: Create EmailJS Account
1. Go to https://emailjs.com
2. Click "Sign Up" → Create account with dukaansetu@gmail.com
3. Verify your email

## Step 2: Add Gmail Service
1. In EmailJS dashboard → "Email Services" → "Add New Service"
2. Choose "Gmail" 
3. Connect your dukaansetu@gmail.com account
4. Copy the **Service ID** (looks like: service_xxxxxxx)

## Step 3: Create Templates

### Template 1: New Subscription Notification (to you)
1. Go to "Email Templates" → "Create New Template"
2. Template ID: `template_subscription_notification`
3. Subject: `New Dukaan Setu Subscription`
4. Content:
```
New subscriber: {{from_email}}

Time: {{message}}

This person subscribed to Dukaan Setu coming soon page.
```

### Template 2: Welcome Email (to subscribers)
1. Create another template
2. Template ID: `template_welcome_email`
3. Subject: `Welcome to Dukaan Setu - Stay Updated!`
4. Content:
```
Welcome to Dukaan Setu!

Thank you for subscribing. You'll be notified with the latest updates about our launch and exciting features.

We're building something amazing to help you discover nearby shops and place orders seamlessly.

Stay tuned for updates!

Best regards,
Dukaan Setu Team
dukaansetu@gmail.com
```

## Step 4: Get Your User ID
1. Go to "Account" → "General"
2. Copy your **Public Key** (User ID)

## Step 5: Update Your HTML
Replace these in your coming soon page:
- `YOUR_EMAILJS_USER_ID` → Your Public Key
- `YOUR_SERVICE_ID` → Your Gmail Service ID
- `YOUR_TEMPLATE_ID` → template_subscription_notification
- `YOUR_WELCOME_TEMPLATE_ID` → template_welcome_email

## Step 6: Test
1. Upload your HTML to hosting (Netlify/Vercel)
2. Test the subscription form
3. Check dukaansetu@gmail.com for notifications
4. Check subscriber's email for welcome message

## Ready-to-Use Code
Your HTML is already updated with the correct email templates. Just replace the placeholder IDs!

## Troubleshooting
- Make sure Gmail service is connected properly
- Check browser console for errors
- Verify template IDs match exactly
- Test with a real email address
