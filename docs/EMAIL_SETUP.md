# Contact Form Setup Instructions

The contact form is now ready to be functional, but requires EmailJS configuration to send emails.

## EmailJS Setup Guide

### Step 1: Create EmailJS Account
1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Sign up for a free account (up to 200 emails/month)
3. Verify your email address

### Step 2: Connect Email Service
1. In EmailJS dashboard, go to "Email Services"
2. Click "Add Service"
3. Choose your email provider (Gmail, Outlook, etc.)
4. Follow the setup instructions for your provider
5. Note down your **Service ID**

### Step 3: Create Email Template
1. Go to "Email Templates" in EmailJS dashboard
2. Click "Create New Template"
3. Use this template structure:

```
Subject: New Contact Form Submission - {{from_name}}

From: {{from_name}} ({{from_email}})
Company: {{company}}

Message:
{{message}}

---
This message was sent from Victory International Trading website contact form.
```

4. Save the template and note down your **Template ID**

### Step 4: Get Public Key
1. Go to "Account" > "General" in EmailJS dashboard
2. Copy your **Public Key**

### Step 5: Update Website Code
In `index.html`, replace these placeholders:

```javascript
// Line 937: Replace with your public key
emailjs.init("YOUR_PUBLIC_KEY");

// Lines 1055-1059: Replace with your IDs
const result = await emailjs.sendForm(
    'YOUR_SERVICE_ID',    // Your EmailJS service ID
    'YOUR_TEMPLATE_ID',   // Your EmailJS template ID
    this,
    'YOUR_PUBLIC_KEY'     // Your EmailJS public key
);
```

### Example Configuration
```javascript
// Example (replace with your actual values)
emailjs.init("user_abcd1234efgh5678");

const result = await emailjs.sendForm(
    'service_gmail_123',
    'template_contact_456',
    this,
    'user_abcd1234efgh5678'
);
```

## Form Features

### ✅ What's Already Implemented
- **Form Validation**: Required fields, email format validation
- **Loading States**: Button shows spinner during submission
- **Success/Error Messages**: User feedback for form submission
- **Field Error Display**: Individual field error messages
- **Responsive Design**: Works on all devices
- **Accessibility**: Proper labels and error associations

### 🔧 Form Fields
- **Name** (required)
- **Email** (required, validated)
- **Company** (optional)
- **Message** (required)

### 📱 User Experience
1. Form validates on submission
2. Shows loading spinner while sending
3. Displays success message on successful submission
4. Shows error message if submission fails
5. Clears errors as user types
6. Form resets after successful submission

## Testing the Form

### Without EmailJS Setup
- Form validation will work
- Loading state will show
- Error message will display (since EmailJS is not configured)

### With EmailJS Setup
- Complete functionality including email delivery
- Success messages on successful submissions

## Alternative Email Solutions

If you prefer not to use EmailJS, here are other options:

### Option 1: Formspree
- Add `action="https://formspree.io/f/YOUR_FORM_ID"` to form
- Remove EmailJS JavaScript
- Simple setup, no JavaScript required

### Option 2: Netlify Forms
- Add `netlify` attribute to form
- Works automatically if hosting on Netlify

### Option 3: PHP Backend
- Create `contact.php` file with mail() function
- Requires PHP hosting
- More control but needs server-side setup

## Support

For EmailJS-specific issues, refer to:
- [EmailJS Documentation](https://www.emailjs.com/docs/)
- [EmailJS Getting Started Guide](https://www.emailjs.com/docs/tutorial/creating-contact-form/)

The form is fully functional once EmailJS is configured with your credentials.