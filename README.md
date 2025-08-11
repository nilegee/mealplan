# Mariem's Kitchen Planner - Authentication System

## Overview
This meal planning application now includes Supabase authentication with user whitelisting to restrict access to authorized family members only.

## Authorized Users

### Regular Users
- `yazidgeemail@gmail.com` - Yazid (user role)
- `yahyageemail@gmail.com` - Yahya (user role)

### Administrators  
- `abdessamia.mariem@gmail.com` - Mariem (admin role)
- `nilezat@gmail.com` - Admin (admin role)

## Authentication Features

### Sign In
- Email and password authentication via Supabase
- Only whitelisted emails can successfully authenticate
- Failed attempt tracking with security lockout

### Sign Up
- New account creation for whitelisted emails only
- Password validation (minimum 8 characters)
- Email verification required

### Security Features
- **Rate Limiting**: Maximum 5 failed login attempts
- **Temporary Lockout**: 15-minute lockout after too many failed attempts
- **Email Validation**: Emails are normalized and validated
- **Session Management**: Automatic logout of unauthorized users
- **Data Protection**: Sensitive data cleared on logout

## How It Works

1. **Initial Load**: User sees authentication screen
2. **Login Attempt**: User enters email and password
3. **Validation**: System checks if email is whitelisted
4. **Authentication**: Supabase handles password verification
5. **Access Control**: Only successful + whitelisted users access main app
6. **Session Persistence**: User stays logged in between visits
7. **Automatic Logout**: Unauthorized users are automatically signed out

## Technical Implementation

- **Supabase Integration**: Uses provided project credentials
- **Client-Side Protection**: Main app content hidden until authenticated
- **User Role Display**: Shows user name and role in header
- **Error Handling**: Clear error messages for authentication failures
- **Progressive Enhancement**: Graceful degradation if external resources fail

## Usage Instructions

1. Navigate to the application
2. Enter your authorized email and password
3. Click "Sign In" (or "Create Account" for first time)
4. Upon successful authentication, access the full meal planning features
5. Use "Sign Out" button in header to logout securely

## Contact
For access requests or issues, contact the administrator at the provided admin emails.