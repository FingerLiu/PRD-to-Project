# Mobile App Publishing Guide
**TODO**

This guide covers the process of publishing your AI-generated mobile application to the App Store (iOS) and Google Play Store (Android).

## Prerequisites

- Completed mobile application
- Developer accounts
  - Apple Developer Account ($99/year)
  - Google Play Developer Account ($25 one-time)
- App signing certificates
- Privacy policy and terms of service

## iOS App Store Publishing

### 1. Preparation

```bash
# Install latest Xcode
xcode-select --install

# Install CocoaPods (if using)
sudo gem install cocoapods
```

### 2. App Store Connect Setup

1. Create app in App Store Connect
2. Configure app information
   - App name
   - Bundle ID
   - SKU
   - Privacy policy URL

### 3. Build Configuration

```bash
# Update version and build number
/usr/libexec/PlistBuddy -c "Set :CFBundleShortVersionString 1.0.0" Info.plist
/usr/libexec/PlistBuddy -c "Set :CFBundleVersion 1" Info.plist
```

### 4. Archive and Upload

1. In Xcode:
   - Select "Generic iOS Device"
   - Product > Archive
   - Validate App
   - Upload to App Store

## Google Play Store Publishing

### 1. Preparation

```bash
# Generate signed APK/Bundle
./gradlew bundleRelease
```

### 2. Play Console Setup

1. Create app in Play Console
2. Configure app information
   - App name
   - Package name
   - Category
   - Content rating

### 3. Release Types

1. **Internal Testing**
   - Limited to specific testers
   - Quick approval process
   - Instant updates

2. **Closed Testing**
   - Private group testing
   - Limited public testing
   - Beta feedback

3. **Open Testing**
   - Public beta testing
   - Staged rollout
   - Feature testing

4. **Production**
   - Full public release
   - Phased rollout
   - Monitor metrics

## App Store Optimization (ASO)

### 1. Metadata Optimization

```yaml
title:
  length:
    ios: "30 characters"
    android: "50 characters"
  keywords: "relevant, searchable, terms"

description:
  length:
    ios: "4000 characters"
    android: "7000 characters"
  structure:
    - Features
    - Benefits
    - Social proof
    - Call to action
```

### 2. Visual Assets

- App icon
- Screenshots
- Preview video
- Feature graphic (Android)

## Compliance and Security

### 1. iOS Requirements

- App Privacy Details
- IDFA Declaration
- Export Compliance
- Content Rights

### 2. Android Requirements

- Data Safety Form
- Content Rating
- Target API Level
- Play Protect

## Release Checklist

### 1. Pre-submission
- [ ] App fully tested
- [ ] Crashlytics configured
- [ ] Analytics implemented
- [ ] Deep links verified
- [ ] Push notifications tested

### 2. Store Listing
- [ ] Screenshots prepared
- [ ] Description optimized
- [ ] Privacy policy updated
- [ ] Support URL active
- [ ] Marketing URL ready

### 3. Technical
- [ ] Signing certificates secured
- [ ] API endpoints production-ready
- [ ] Third-party SDKs updated
- [ ] Performance optimized
- [ ] Security reviewed

## Common Issues

### 1. Rejection Reasons
- Missing privacy policy
- Crash on launch
- Incomplete metadata
- Performance issues
- Content violations

### 2. Solutions
- Review guidelines thoroughly
- Test extensively
- Document features clearly
- Respond promptly
- Appeal if necessary

## Best Practices

1. **Version Management**
   - Semantic versioning
   - Clear changelog
   - Beta testing
   - Phased rollout

2. **Quality Assurance**
   - Automated testing
   - Manual testing
   - Device compatibility
   - Network conditions

3. **User Feedback**
   - Monitor reviews
   - Respond to feedback
   - Regular updates
   - Clear communication

## Related Resources

- [Web App Deployment](./deploy-web.md)
- [Mini Program Release](./deploy-miniprogram.md)
- [Custom Templates](./custom-templates.md)
